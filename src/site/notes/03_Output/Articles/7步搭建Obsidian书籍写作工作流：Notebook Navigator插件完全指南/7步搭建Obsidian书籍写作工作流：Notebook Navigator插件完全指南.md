---
{"dg-publish":true,"permalink":"/03-output/articles/7-obsidian-notebook-navigator/7-obsidian-notebook-navigator/","title":"7步搭建Obsidian书籍写作工作流：Notebook Navigator插件完全指南","tags":["插件","PluginTutorial"],"dg-note-properties":{"object":"Article","object_cn":"文章","object_abbr":"ART","category":"Content","category_cn":"内容输出","status":["reviewing"],"metadata_version":"2.0","created":"2026-09-08","updated":"2026-09-08","directory":"03_Output/Articles","title":"7步搭建Obsidian书籍写作工作流：Notebook Navigator插件完全指南","summary":"","tags":["插件","PluginTutorial"],"area":"知识管理","word_count":0,"reading_time":0,"publish_status":"draft","publish_date":null,"primary_platform":"微信公众号","publish_platforms":[],"publish_url":"","views":0,"likes":0,"comments":0,"collections":0,"progress":0,"archived":false,"related_notes":[],"related_products":[],"new_user":0,"readers":0,"shares":0,"avg_read_time":0,"completion_rate":0,"sort_index":33500}}
---

![7步搭建Obsidian书籍写作工作流：Notebook Navigator插件完全指南.jpg](/img/user/03_Output/Articles/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97.jpg)

# 7步搭建Obsidian书籍写作工作流：Notebook Navigator插件完全指南

最近开始着手，计划开始写第二本书，第一本数据分析书的时候，刚开始接触Obsidian，使用的插件是Project+Dataview，有很多不方便的地方，只能通过项目文件夹来逐步添加内容，通过Project来可视化管理，Dataview来进行字数统计等。

写作过程中，不同的需求环境都需要不断切换，尤其是不同章节的顺序调整，需要手动，字数查看需要跳转到不同的统计页面，还是很影响写作过程的专注度。

最近解锁了一个Notebook Navigator插件后，发现除了日历和导航等功能，用来写书、写教程其实非常的好用并顺滑，以前写书遇到的哪些问题其实都解决了。

在进一步熟悉和盘点评估功能之后，发现在插件内部完全可以形成一条非常适合写书的工作流。实现如下核心功能：

1. 绑定快捷方式入口
2. 快速修改章节名称
3. 快速调整章节顺序
4. 快速标记章节状态
5. 快速合并章节笔记
6. 快速新增分组及标题
7. 实时章节字数进度统计

通过以上工作流，实现了写作入口、标题、顺序、状态、合并、分组、统计等形成写书完整的一个工作流程，不用再借助任何插件和功能，去补充写书过程中想要了解和做的事情。

## 1、绑定快捷方式入口

在Obsidian的项目文件下，建立一个写书项目名称，比如：Obsidian知识管理，然后点击左上角的Notebook Navigator插件图标，找到项目文件：Obsidian知识管理，点击右键，添加到快捷方式。

![7步搭建Obsidian书籍写作工作流：Notebook Navigator插件完全指南-10.png\|238](/img/user/03_Output/Articles/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97-10.png)

添加完成以后，在图标正下方的快捷方式位置，就可以看到文件已经添加到快捷方式了。

![03_Output/Articles/7步搭建Obsidian书籍写作工作流：Notebook Navigator插件完全指南/7步搭建Obsidian书籍写作工作流：Notebook Navigator插件完全指南.png\|222](/img/user/03_Output/Articles/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97.png)

后续每次写书，点开插件双导航形态，点击快捷文件夹，可以直接看到章节，并选中章节，直接进入写作状态中。

![7步搭建Obsidian书籍写作工作流：Notebook Navigator插件完全指南-11.png](/img/user/03_Output/Articles/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97-11.png)

## 2、快速修改章节名称

当进入Notebook Navigator插件的双导航栏，进入写作后，可以随时添加笔记，并且修改笔记章节名称。

![7步搭建Obsidian书籍写作工作流：Notebook Navigator插件完全指南-12.png\|399](/img/user/03_Output/Articles/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97-12.png)

通过这种方式，再也不用每个笔记承担太多的写作压力和任务，每次通过新建一个笔记，只写一个小节内容，随时新建对应的笔记名称作为新的标题。

## 3、快速调整章节顺序

随着你的小节越来越多，势必会要调整小节的顺序，可以通过点击手动排序功能，随后会跳出确认框，点击确认后，再选择对应的编辑排序，就可以拖动笔记进行人工自定义排序了。
![7步搭建Obsidian书籍写作工作流：Notebook Navigator插件完全指南-13.png\|403](/img/user/03_Output/Articles/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97-13.png)

在排序后，就可以按照书的框架顺序排列，有新的小节就再进行添加调整顺序即可。
![7步搭建Obsidian书籍写作工作流：Notebook Navigator插件完全指南-14.png\|402](/img/user/03_Output/Articles/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97-14.png)
当排序之后，可以看到插件自动生成了一个sort_index字段，通过这个随时自动更新这个值，来进行顺序自动调整。

## 4、快速标记章节状态

不同的小节可能随时有调整，有的已经不需要修改了，可以通过属性标记状态完成，有的可以设置属性状态撰写中。因此，需要有一个状态调整的功能。

Notebook Navigator为了更方便的管理不同章节的完成状态，可以实现属性状态快速调整。在插件左侧文件夹导航部分，拉倒最下面有属性，设置打开使用这个功能，可以通过选中右侧笔记拖拉到对应属性处，直接更改属性，不用再通过点击笔记上放的属性区域，去手动添加字段和对应状态值。

首先要启动这个功能，通过设置，打开插件配置页面，可以马上看到配置属性键，如下：

![7步搭建Obsidian书籍写作工作流：Notebook Navigator插件完全指南-2.png\|356](/img/user/04_Product/Projects/%E5%86%99%E4%B9%A6%E9%A1%B9%E7%9B%AE/%E6%89%8B%E5%8A%A8%E6%8E%92%E5%BA%8F%E5%8A%9F%E8%83%BD/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97-2.png)

点击打开后，搜索status，勾选导航、清单、文件夹都可视化，如下：

![04_Product/Projects/写书项目/手动排序功能/7步搭建Obsidian书籍写作工作流：Notebook Navigator插件完全指南.png\|395](/img/user/04_Product/Projects/%E5%86%99%E4%B9%A6%E9%A1%B9%E7%9B%AE/%E6%89%8B%E5%8A%A8%E6%8E%92%E5%BA%8F%E5%8A%9F%E8%83%BD/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97.png)
应用后，就可以看到左侧文件夹导航显示了这个属性字段，打开折叠可以看到草稿，writing，reviewing等属性，如果要修改，直接拖动笔记到发布或者写作中，笔记自动就会修改成对应的属性，当然也可以直接通过选中单个笔记，或者多个笔记，右键找到status字段，直接进行标识。
![7步搭建Obsidian书籍写作工作流：Notebook Navigator插件完全指南-15.png\|222](/img/user/03_Output/Articles/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97-15.png)

随时的状态更新标识，提高了写书过程的流畅度和专注力，同时也让写作管理更加便捷，不容易受到干扰。


## 5、快速合并章节笔记

当你写完第一章的小节后，希望对多个小节进行合并，形成一个第一章的完整内容，插件也有合并内容的功能。

以下就是通过点击右键，选择合并功能，生成了《第一章完整章节》内容，包含1.1-1.3的笔记所有内容。

![7步搭建Obsidian书籍写作工作流：Notebook Navigator插件完全指南-16.png\|364](/img/user/03_Output/Articles/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97-16.png)

通过合并的功能可以方便形成完整的书籍内容，随时可以导出成为PDF进行发布或者分享，对于写别的内容也可以使用这个功能。

## 6、快速新增分组及标题

一本书一般最少也有多个大章节，或者分为上部、中部和下部，因此，有一个分组折叠功能，在可视化分层管理过程中，是更方便管理的。

依旧选中要分组的第一个笔记，通过右键点击更改分组标题，新建标题、图标、颜色即可。

![7步搭建Obsidian书籍写作工作流：Notebook Navigator插件完全指南-17.png](/img/user/03_Output/Articles/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97-17.png)

可见，随着章节越来越多，分组折叠管理和可视化都会更清晰。

## 7、实时章节字数进度统计

在写书的过程中，篇幅管理过去一直是我考虑的一个问题，避免篇幅太短，内容不够详细清晰，又不想篇幅太长，太多繁琐不重要内容可以精简，这时有个实时统计的字数和进度数据，可以更好的协助管理写作过程。

Notebook Navigator插件专门在章节分组的基础上，可以统计章节的字数目标和当前进度占比。

功能在右键，更改分组标题一起。打开显示数字，设置章节目标字数即可。

![7步搭建Obsidian书籍写作工作流：Notebook Navigator插件完全指南-18.png](/img/user/03_Output/Articles/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97/7%E6%AD%A5%E6%90%AD%E5%BB%BAObsidian%E4%B9%A6%E7%B1%8D%E5%86%99%E4%BD%9C%E5%B7%A5%E4%BD%9C%E6%B5%81%EF%BC%9ANotebook%20Navigator%E6%8F%92%E4%BB%B6%E5%AE%8C%E5%85%A8%E6%8C%87%E5%8D%97-18.png)

## 总结

基于写书过程中会遇到的各种常见问题，都可以通过Notebook Navigator插件的功能，形成一个完整的书籍写作工作流，让写作可以更加顺畅自如。

不再需要考虑任何影响，保持一个持续创作积累，可以更轻松的去完成书籍写作环节。当然Notebook Navigator还有很多好用的功能，可以进一步优化工作流，后续有新的迭代，再持续分享。




**关于我**

西湖太极熊 | 一人公司实践者

持续研究AI个人数据资产洞察和AI+Obsidian知识管理
