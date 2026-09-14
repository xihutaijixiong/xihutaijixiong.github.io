---
{"dg-publish":true,"permalink":"/03-output/articles/workbuddy-obsidian/work-buddy-obsidian/","title":"如何用WorkBuddy+Obsidian分析阅读笔记，输出个人知识资产报告","tags":["AIExperiment","方法论"],"dg-note-properties":{"object":"Article","object_cn":"文章","object_abbr":"ART","category":"Content","category_cn":"内容输出","status":["published"],"metadata_version":"2.0","created":"2026-07-10 14:30:00","updated":"2026-07-10 14:30:00","directory":"03_Output/Articles","title":"如何用WorkBuddy+Obsidian分析阅读笔记，输出个人知识资产报告","summary":"","tags":["AIExperiment","方法论"],"area":"知识管理","word_count":0,"reading_time":0,"publish_status":"draft","publish_date":"2026-08-18","primary_platform":"微信公众号","publish_platforms":[],"publish_url":"","views":122,"likes":4,"comments":0,"collections":6,"progress":0,"archived":false,"related_notes":[],"related_products":[],"new_user":1,"readers":124,"shares":19,"avg_read_time":0.4,"completion_rate":0.32,"sort_index":28000}}
---

# 标题：如何用WorkBuddy+Obsidian分析阅读笔记，输出个人知识资产报告

最近看到WorkBuddy可以做各种好看的工作台，因此也研究了一下，但是我不是想去做工作台，而是希望通过WorkBuddy看看这个模型分析我的数据资产输出质量怎么样，分析后发现，不但质量可以，重点是输出的分析报告是以网页的可视化形式展示。

## 阅读笔记资产主题分析Prompt

因此，在了解了WorkBuddy之后，通过已经沉淀好的105篇阅读笔记数据资产来进行分析，希望可以通过以下Prompt分析一下：

```
你是一名个人知识资产分析师。

根据我的105本阅读数据生成的11个json文件，生成我的个人知识资产报告。

阅读数据json文件名称为:insights json file. 

分析：

1. 阅读行为
2. 兴趣变化
3. 知识结构
4. 核心认知
5. 能力模型
6. 行动影响
7. 未来建议

要求：
不要简单罗列书籍。
寻找长期趋势和隐藏模式。
```

然后，就可以生成一个网页版本的分析报告。

![03_Output/Articles/Workbuddy+Obsidian阅读笔记个人知识资产报告/插图1.png](/img/user/03_Output/Articles/Workbuddy+Obsidian%E9%98%85%E8%AF%BB%E7%AC%94%E8%AE%B0%E4%B8%AA%E4%BA%BA%E7%9F%A5%E8%AF%86%E8%B5%84%E4%BA%A7%E6%8A%A5%E5%91%8A/%E6%8F%92%E5%9B%BE1.png)

![03_Output/Articles/Workbuddy+Obsidian阅读笔记个人知识资产报告/插图2.png](/img/user/03_Output/Articles/Workbuddy+Obsidian%E9%98%85%E8%AF%BB%E7%AC%94%E8%AE%B0%E4%B8%AA%E4%BA%BA%E7%9F%A5%E8%AF%86%E8%B5%84%E4%BA%A7%E6%8A%A5%E5%91%8A/%E6%8F%92%E5%9B%BE2.png)

整体排版不得不说，非常美观，报告整体质量也非常好。

## 可拓展主题

未来想重点分享的不是这个报告，而是数据资产才是最关键的，因为，有了这个数据资产才能从不同的角度去分析，得到不同维度有价值的东西。

比如：

1. 个人知识资产全景分析：知识地图、主题分布、兴趣变化、核心领域
2. 个人思想体系生成：世界观、价值观、核心原则、反常识观点
3. 能力资产分析：能力模型、优势领域、短板
4. 知识框架提炼：框架、模型、方法论库
5. 行动转化分析：行动案例、实践路径、未转化知识
6. 内容资产生成：内容主题、100个选题、栏目规划
7. AI时代资产战略：AI增强方向、产品机会
8. 个人品牌产品分析：定位、用户、产品、收入模型

以上这些都可以不断的设计成skill，来形成不同价值的输出。

## 数据资产是核心

为了将来可以持续的通过不同的AI进行分析，需要先生成数据资产，那阅读笔记的数据资产要如何设计并生成呢？

建议如下步骤：

1. 阅读笔记同步：在Obsidian下载安装weread插件同步阅读笔记到Obsidian固定文件中
2. 数据资产设计：将每一本书的笔记生成一个如下结构生成json文件

```
[
{

"book_info":{

"book_id":"",
"title":"",
"author":"",
"isbn":""

},


"reading_metadata":{

"reading_date":"",
"finished_date":"",
"last_read_date":"",

"reading_time":"",
"progress":"",

"note_count":0,
"review_count":0

},


"engagement_analysis":{

"engagement_level":
"high/medium/low",

"reason":
"根据阅读时间、完成度、笔记数量判断"

},


"knowledge_analysis":{


"knowledge_domains":[

"领域1",
"领域2"

],


"key_concepts":[

{

"concept":"",

"importance":
"high/medium/low",

"evidence":
"来自用户划线内容的依据"

}

],


"core_insights":[

{

"insight":"",

"type":
"认知/方法/案例/行动",

"application":
"可能应用场景"

}

],


"user_attention_patterns":[

"用户关注的问题"

],


"transferable_methods":[

"可迁移的方法"

]


},


"future_tags":[

"商业认知",
"AI",
"职业发展"

],


"content_creation_topics":[

"未来可以生成的内容主题"

]


}

]
```

3. 数据资产skill：按照输出格式，进行skill设计，重点注意避免上下文超过限制，可以每次生成10本数据笔记成json格式，可以提高效率和降低AI分析成本

# 总结

先通过同步阅读笔记到Obsidian，再通过skill生产数据资产，然后通过workbuddy来进行主题分析，生成美观的分析报告。当然通过不同的AI工具一样可以进行分析。

对于各种涉及的skill和模版我都会放在我的网站，免费分享，有需要的可以去网站下载。
> **网站链接:https://xihutaijixiong.github.io/taichi-bear/

--END--