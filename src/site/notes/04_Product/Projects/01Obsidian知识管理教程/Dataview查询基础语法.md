---
{"dg-publish":true,"permalink":"/04-product/projects/01-obsidian/dataview/","tags":["PluginTutorial"],"dg-note-properties":{"sort_index":38000,"group_header":{"title":"Dataview","show_word_count":true,"target_word_count":10000,"icon":"database-search","color":"#84cc16"},"tags":["PluginTutorial"]}}
---

在 Dataview 中，一个**完整**的Dataview查询语法通常包含以下几个核心部分。以下是一个整理好了的，最常用的完整结构，了解每个字段就可以用来查询大部分的笔记维度数据。

### 完整查询语法结构模板

````markdown
```dataview
TABLE 
   file.link AS "文件",           -- 显示字段（可包含计算）
   length(file.outlinks) AS "外链数", -- 统计字段
   date(now) - file.cday AS "存在天数" -- 计算字段
FROM 
   "笔记文件夹"                   -- 来源（也可以写 #tag）
WHERE 
   file.cday >= date(today) - dur(7 days) -- 过滤条件
   AND file.name != "模板"       -- 多条件用 AND/OR
GROUP BY 
   file.folder                   -- 按文件夹分组
FLATTEN 
   file.tags AS tag              -- 展开列表字段（可选）
SORT 
   file.mtime DESC               -- 排序（DESC降序/ASC升序）
LIMIT 
   50                            -- 限制返回行数（可选）
```
````

---

### 逐行详细解释

| 关键字 | 作用 | 说明 |
| :--- | :--- | :--- |
| **`TABLE`** | **定义输出列** | 指定要显示的字段。可以用 `AS` 重命名列标题。如果不写字段，默认显示文件名。 |
| **`FROM`** | **指定数据来源** | 可以写文件夹路径（`"文件夹"`）、标签（`#标签`）或链接（`[[页面]]`）。`from ""` 表示全库搜索。 |
| **`WHERE`** | **过滤行数据** | 只保留满足条件的笔记。支持逻辑运算（`AND`、`OR`）和日期/文本比较。 |
| **`GROUP BY`** | **分组聚合** | 按照某个字段（如文件夹、标签）将笔记分组。分组后通常配合 `length()`、`sum()` 等聚合函数使用。 |
| **`FLATTEN`** | **展开数组字段** | 将列表类型的字段（如 `file.tags`、`file.outlinks`）展开，让每个元素单独成行（不常用，但处理多值字段时必须用）。 |
| **`SORT`** | **排序结果** | 按某个字段升序（`ASC`）或降序（`DESC`）排列。默认是 `ASC`。 |
| **`LIMIT`** | **限制行数** | 只返回前 N 条记录，用于性能优化或只看 Top N。 |

---

### 一个带“分组统计”的实用示例

假设你想**按文件夹分组**，统计每个文件夹下有多少篇笔记，并显示最新的修改时间：

````markdown
```dataview
TABLE 
   length(rows) AS "笔记数量",                       -- 统计每组行数
   max(rows.file.mtime) AS "最新修改时间"            -- 每组内最新的时间
FROM ""
WHERE 
   file.folder != ""                              -- 排除根目录（可选）
GROUP BY 
   file.folder AS "文件夹"
SORT 
   length(rows) DESC                              -- 按笔记数量降序排列
```
````

> **关键点**：分组后，`rows` 代表“组内所有笔记的集合”。需要用 `rows.字段` 的方式访问组内数据，并用 `length()`、`max()`、`min()` 等聚合函数来统计。

---

### 注意事项（避坑指南）

1. **`rows` 只在分组后可用**：如果使用了 `GROUP BY`，输出列必须使用 `rows.xxx` 或聚合函数。
2. **日期比较格式**：日期必须用 `date()` 包裹，如 `date(today)` 或 `date("2026-09-04")`。
3. **字段名前缀**：系统字段（`file`、`date` 等）前不加前缀，自定义 frontmatter 字段（如 `评分`）直接写字段名即可。
4. **性能问题**：如果库很大，`FROM ""` 会遍历全部笔记，建议尽量用 `FROM "文件夹"` 缩小范围。
