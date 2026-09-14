---
{"dg-publish":true,"permalink":"/03-output/articles/grok/grok-prompt-ai-obsidian-10/","title":"Grok免费版从零搭建资讯雷达：附完整prompt模板，以AI+Obsidian行业为例，每天10分钟过滤高质量信息","dg-note-properties":{"object":"Article","object_cn":"文章","object_abbr":"ART","category":"Content","category_cn":"内容输出","status":["published"],"metadata_version":"2.0","created":"2026-08-28","updated":"2026-08-28 14:30:00","directory":"03_Output/Articles","title":"Grok免费版从零搭建资讯雷达：附完整prompt模板，以AI+Obsidian行业为例，每天10分钟过滤高质量信息","summary":"","tags":[],"area":"知识管理","word_count":0,"reading_time":0,"publish_status":"draft","publish_date":"2026-09-09","primary_platform":"微信公众号","publish_platforms":[],"publish_url":"","views":0,"likes":0,"comments":0,"collections":0,"progress":0,"archived":false,"related_notes":[],"related_products":[],"new_user":0,"readers":0,"shares":0,"avg_read_time":0,"completion_rate":0}}
---

![插图0封面.png](/img/user/03_Output/Articles/Grok%E5%85%8D%E8%B4%B9%E7%89%88%E4%BB%8E%E9%9B%B6%E6%90%AD%E5%BB%BA%E8%B5%84%E8%AE%AF%E9%9B%B7%E8%BE%BE/%E6%8F%92%E5%9B%BE0%E5%B0%81%E9%9D%A2.png)

# 标题：Grok免费版从零搭建资讯雷达：附完整prompt模板，以AI+Obsidian行业为例，每天10分钟过滤高质量信息

一直在探索如何可以让AI更高效的帮我进行每日信息筛选并输入到Obsidian，但是尝试过付费的chatgpt或者通过Agent成本还是太高，尤其是你的输入方案不够精细，即使AI能实现，你不在乎成本，筛选后的内容质量和相关新也不会太好。

在不断寻找和尝试后，找到一个AI平台Grok，可以通过免费版Grok来实现输入，通过从零搭建资讯雷达，实现通过prompt，每天只需要不到10分钟，Grok就可以输出一个关于我一直在研究的，AI+Obsidian行业相关的信息报告。

## 为何选择GroK?

![03_Output/Articles/Grok免费版从零搭建资讯雷达/插图1.png](/img/user/03_Output/Articles/Grok%E5%85%8D%E8%B4%B9%E7%89%88%E4%BB%8E%E9%9B%B6%E6%90%AD%E5%BB%BA%E8%B5%84%E8%AE%AF%E9%9B%B7%E8%BE%BE/%E6%8F%92%E5%9B%BE1.png)

由于希望获取的输入信息是最前沿的，也是质量比较高的一手信息，因此，最后选择了Grok是有原因的。因为**Grok 的训练数据深度依赖 X 平台（原 Twitter）**，同时也积极引入其他来源（如：油管、Reddit等）以增强其能力。

在深度了解Grok会发现其来源信息中，X 平台的**公开用户数据是 Grok 的核心训练语料**，包括公开的帖子、互动、个人简介等。它的实时搜索和回答大量依赖于X上正在发生的讨论，因此，获取的信息都是最前沿的一手信息输入，可以给到你最大的参考和启发。

此外，Grok 的训练数据来源还在不断扩展。除了X，它也会抓取**公开的网页信息**。更重要的是，其开发公司xAI正积极引入**独家的高质量数据**。

因此，对于免费版本就可以获取更多的在X和其他平台能获取的一手信息，就可以满足大部分人的需求，所以才选择了Grok。

插图：Grok截图即可。

## 如何从零搭建资讯雷达？

如果仅仅有了平台，还无法高效的获取有质量的输入，需要从需求到背景，到搜索原则和类别等进行详细规范，才能尽可能的提高AI获取更高质量输入信息。

就以我致力于终身探索的AI+Obsidian为例，我的初步需求是：

```
请基于最新、真实、可验证的一手信息，帮助我发现过去 24–72 小时内最值得我关注的AI+Obsidian相关内容；如果过去 24–72 小时内容不足，可以扩大到最近 7 天，但必须明确标注发布时间。
```

对于这个需求要建立一个搜索框架，如下：

1. 背景：说明清楚你的能力、兴趣和研究方向
2. 搜索原则：说明清楚你的搜索平台和范围优先级，降低二手信息和垃圾文章比例
3. 时间要求：灵活自定义搜索时间范围
4. 搜索类别：圈定搜索类别，比如：知识管理、AI洞察、AI工作流等
5. 类别输出定义：不要有多少输出多少，尽可能对每个类别缩小范围
6. 搜索输出格式：给出信息来源标题、类型、来源、URL、一句话总结等，方便后续人工评估
7. 行动建议：对于输入的信息，结合个人背景给出建议行动
8. 质量控制：约束内容，减少无效的输入，比如：所有链接必须可以直接打开

![03_Output/Articles/Grok免费版从零搭建资讯雷达/插图2.png](/img/user/03_Output/Articles/Grok%E5%85%8D%E8%B4%B9%E7%89%88%E4%BB%8E%E9%9B%B6%E6%90%AD%E5%BB%BA%E8%B5%84%E8%AE%AF%E9%9B%B7%E8%BE%BE/%E6%8F%92%E5%9B%BE2.png)

## 输出案例报告

在根据自己的需求建立Prompt之后，直接给Grok进行分析输出，就可以得到相对范围内，最接近你探索内容的一手高质量内容。

如下报告，首先给出了今日分析的最重要的5个信号，对于当前AI和Obsidian发展，Obsidian正在快速变成AI Agent的本地前端，证明知识管理越来越重要，并且未来会趋向于变成Agent可续写的工作区，这也是我一直坚定的方向。

报告的5个个信息如下图：
![03_Output/Articles/Grok免费版从零搭建资讯雷达/插图3.png](/img/user/03_Output/Articles/Grok%E5%85%8D%E8%B4%B9%E7%89%88%E4%BB%8E%E9%9B%B6%E6%90%AD%E5%BB%BA%E8%B5%84%E8%AE%AF%E9%9B%B7%E8%BE%BE/%E6%8F%92%E5%9B%BE3.png)
然后报告会对于不同类型给出top的几篇输入，可以先通过基础的字段信息进行人工评估，觉得对自己最有用和最感兴趣的内容，可以打开进行详细阅读，如果觉得来不及或者希望以后再读，可以直接通过Obsidian Web Clipper剪藏到Obsidian，未来再阅读或者作为数据资产，通过AI进一步分析也可以。

![03_Output/Articles/Grok免费版从零搭建资讯雷达/插图4.png](/img/user/03_Output/Articles/Grok%E5%85%8D%E8%B4%B9%E7%89%88%E4%BB%8E%E9%9B%B6%E6%90%AD%E5%BB%BA%E8%B5%84%E8%AE%AF%E9%9B%B7%E8%BE%BE/%E6%8F%92%E5%9B%BE4.png)

不同的分类下有2-3篇优质雷达识别输出，最后会综合评估，给出最值得阅读的Top5内容，如果时间不足，可以直接看这个Top5内容。
![03_Output/Articles/Grok免费版从零搭建资讯雷达/插图5.png](/img/user/03_Output/Articles/Grok%E5%85%8D%E8%B4%B9%E7%89%88%E4%BB%8E%E9%9B%B6%E6%90%AD%E5%BB%BA%E8%B5%84%E8%AE%AF%E9%9B%B7%E8%BE%BE/%E6%8F%92%E5%9B%BE5.png)

报告除了给出输出内容，还会从多个维度进行分析，给出一些商机评估，比如：

1. AI 正在从“帮我写笔记”转向“理解并维护我的整个知识库”
2. 一人公司的高收入案例集中在垂直、可量化交付的 AI 产品，而不是通用 PKM。
3. 用户愿意为“减少重复解释 + 保持更新责任”付钱/花时间。

## 总结

通过以上的Prompt进行AI实验，发现给出的内容质量和商机评估都非常值得学习。不同的人结合自己的不同需求，完全可以进一步修改Prompt找到适合自己的方案设计。

这套Prompt方案的核心在于框架，而非工具。如果您觉得这个思路对您有启发，可以回复：**雷达**，我可以将这份Prompt模板无偿分享，您稍作修改即可适配自己的领域。
