---
{"dg-publish":true,"permalink":"/03-output/articles/3-obsidian-apex-dashboard/3-obsidian-apex-dashboard/","title":"3步用Obsidian Apex Dashboard插件，搭建项目和实验协同工作台（附配置模板）","tags":["插件","PluginTutorial"],"dg-note-properties":{"object":"Article","object_cn":"文章","object_abbr":"ART","category":"Content","category_cn":"内容输出","status":["reviewing"],"metadata_version":"2.0","created":"2026-09-09","updated":"2026-09-09","directory":"03_Output/Articles","title":"3步用Obsidian Apex Dashboard插件，搭建项目和实验协同工作台（附配置模板）","summary":"","tags":["插件","PluginTutorial"],"area":"知识管理","word_count":0,"reading_time":0,"publish_status":"draft","publish_date":null,"primary_platform":"微信公众号","publish_platforms":[],"publish_url":"","views":0,"likes":0,"comments":0,"collections":0,"progress":0,"archived":false,"related_notes":[],"related_products":[],"new_user":0,"readers":0,"shares":0,"avg_read_time":0,"completion_rate":0,"sort_index":37500}}
---

![3步用Obsidian Apex Dashboard插件，搭建项目和实验协同工作台（附配置模板）.png](/img/user/03_Output/Articles/3%E6%AD%A5%E7%94%A8Obsidian%20Apex%20Dashboard%E6%8F%92%E4%BB%B6%EF%BC%8C%E6%90%AD%E5%BB%BA%E9%A1%B9%E7%9B%AE%E5%92%8C%E5%AE%9E%E9%AA%8C%E5%8D%8F%E5%90%8C%E5%B7%A5%E4%BD%9C%E5%8F%B0%EF%BC%88%E9%99%84%E9%85%8D%E7%BD%AE%E6%A8%A1%E6%9D%BF%EF%BC%89/3%E6%AD%A5%E7%94%A8Obsidian%20Apex%20Dashboard%E6%8F%92%E4%BB%B6%EF%BC%8C%E6%90%AD%E5%BB%BA%E9%A1%B9%E7%9B%AE%E5%92%8C%E5%AE%9E%E9%AA%8C%E5%8D%8F%E5%90%8C%E5%B7%A5%E4%BD%9C%E5%8F%B0%EF%BC%88%E9%99%84%E9%85%8D%E7%BD%AE%E6%A8%A1%E6%9D%BF%EF%BC%89.png)

# 标题：3步用Obsidian Apex Dashboard插件，搭建项目和实验协同工作台（附配置模板）

在研究Obsidian管理项目的时候，一直有个问题没有得到很好的解决，不知道大家是否也遇到同样的问题。

管理一个项目的时候，在项目过程中会涉及很多需要研究的点，比如：开发一个网站项目，一定会涉及后台不同，前台可视化等不同模块，因此，需要分不同模块去研究和实验测试，因此，大项目下就产生了小的子项目。

在Obsidian中管理的过程中，我更愿意称为项目下的小实验，一个个研究实验去解决项目的不同环节，不同子项目问题。但是在过去都是通过链接或者文件管理，很难形成一个类似可视化项目调度工作台的模式，来每天管理推进后续的项目和实验，以及项目中的任务。

最近研究了Apex Dashboard插件，发现终于可以解决这个问题了，可以将Apex Dashboard设计成一个最强工作台，来调度指挥项目推进和落地。

## 管理定位

对于不同的人管理项目可能有各种管理习惯，同时，大型项目也有标准的项目管理SOP，但是作为个人来说，最重要的就是确定项目和目标，然后在实现项目的过程中，可能会按照不同的方式去实现：

1. 按照项目开发流程去实现，比如：开发一个网站项目
2. 按照项目模块去实现：比如：英语学习听、说、读、写
3. 按照项目框架去实现：比如：一人公司系统是一个整体系统框架，需要多个项目按照结构逐步去落地实现

因此，在尝试了各种管理方式之后，建议个人参考项目对应实验的方式去设计（仅供参考）。

## 解决方案

当确认了项目和实验的管理定位思想之后，再思考应用到在Apex Dashboard插件中，去落地实际的管理方案。

![3步用Obsidian Apex Dashboard插件，搭建项目和实验协同工作台（附配置模板）-1.png\|739](/img/user/03_Output/Articles/3%E6%AD%A5%E7%94%A8Obsidian%20Apex%20Dashboard%E6%8F%92%E4%BB%B6%EF%BC%8C%E6%90%AD%E5%BB%BA%E9%A1%B9%E7%9B%AE%E5%92%8C%E5%AE%9E%E9%AA%8C%E5%8D%8F%E5%90%8C%E5%B7%A5%E4%BD%9C%E5%8F%B0%EF%BC%88%E9%99%84%E9%85%8D%E7%BD%AE%E6%A8%A1%E6%9D%BF%EF%BC%89/3%E6%AD%A5%E7%94%A8Obsidian%20Apex%20Dashboard%E6%8F%92%E4%BB%B6%EF%BC%8C%E6%90%AD%E5%BB%BA%E9%A1%B9%E7%9B%AE%E5%92%8C%E5%AE%9E%E9%AA%8C%E5%8D%8F%E5%90%8C%E5%B7%A5%E4%BD%9C%E5%8F%B0%EF%BC%88%E9%99%84%E9%85%8D%E7%BD%AE%E6%A8%A1%E6%9D%BF%EF%BC%89-1.png)

在Apex Dashboard插件中，建立两个分区，一个是项目分区，一个是实验分区。

### 项目分区

对于项目分区主要负责建立项目卡片，点击分区，选择：便利贴，再点击卡片即可。

![3步用Obsidian Apex Dashboard插件，搭建项目和实验协同工作台（附配置模板）-2.png\|317](/img/user/03_Output/Articles/3%E6%AD%A5%E7%94%A8Obsidian%20Apex%20Dashboard%E6%8F%92%E4%BB%B6%EF%BC%8C%E6%90%AD%E5%BB%BA%E9%A1%B9%E7%9B%AE%E5%92%8C%E5%AE%9E%E9%AA%8C%E5%8D%8F%E5%90%8C%E5%B7%A5%E4%BD%9C%E5%8F%B0%EF%BC%88%E9%99%84%E9%85%8D%E7%BD%AE%E6%A8%A1%E6%9D%BF%EF%BC%89/3%E6%AD%A5%E7%94%A8Obsidian%20Apex%20Dashboard%E6%8F%92%E4%BB%B6%EF%BC%8C%E6%90%AD%E5%BB%BA%E9%A1%B9%E7%9B%AE%E5%92%8C%E5%AE%9E%E9%AA%8C%E5%8D%8F%E5%90%8C%E5%B7%A5%E4%BD%9C%E5%8F%B0%EF%BC%88%E9%99%84%E9%85%8D%E7%BD%AE%E6%A8%A1%E6%9D%BF%EF%BC%89-2.png)

比如：知识管理项目，填写清楚项目目标、进展、下一步或者下一阶段要做的事情，列举清楚即可，不需要太多信息。

```
项目目标：建立一套完善的知识管理工作体系
进展：[[知识管理]]
Next：工作台管理课程
```

对于项目进展随时通过链接点击到详细项目进展即可，因为，一个项目可能有多个子项目并行，都可以通过详细项目也面来管理，但是一般当前活跃的子项目实验，后续会在实验区域列举。

此卡片更多的是管理项目和进展和下一步要做的事情，聚焦最重要的这3点即可，工作台信息不宜过多。

### 实验分区

实现分区建立方法和项目一样，但是内容不同。分区内容主要是写清楚实验、状态、属于的项目、重点要解决什么问题，下一步要做的事情。

```
实验：Apex Dashboard管理工作台
状态：[[实验-工作台管理]]
项目：知识管理
Finding：有效可持续的管理方案
Next：撰写工作台管理方案
```

默认添加到实验的都是活跃状态的实验，因此，可以直接放详细实验链接，每天先看当前最紧急的任务，然后再看实验链接去开始推进项目，让你每天10秒即可开始进入执行状态。

> [!info] 提醒
> 1.在实验链接中，可以随时添加任务，汇聚到工作台，后续集中在任务管理介绍中会详细介绍。
2.在以上的项目和实验的链接中是详细的管理模版，每个人都可以按照自己习惯和参考项目标准管理框架进行调整即可，如有需要可以单独告诉我，免费同步分享。

## 总结

通过在工作台设计好工作管理定位和框架，然后一步步按照实验来推进项目落地，实际这更多的是工作流管理层面，在实际落地还是需要通过通过Notebook Navigator管理Markdown来协同，才能最终将解决内容沉淀到Markdown中，完成最后的归档。

后续会进一步补充和完善整个工作台的管理执行工作流，有任何问题随时交流。





**关于我**

西湖太极熊 | 一人公司实践者

持续研究AI个人数据资产洞察和AI+Obsidian知识管理

--END--