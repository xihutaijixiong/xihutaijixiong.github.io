---
{"dg-publish":true,"permalink":"/03-output/articles/obsidian-10-dashboard/obsidian-10-dashboard/","title":"Obsidian新手入门：花10分钟搭建一个最简单实用的Dashboard","tags":["Dashboard","入门教程","插件"],"dg-note-properties":{"object":"Article","object_cn":"文章","object_abbr":"ART","category":"Content","category_cn":"内容输出","status":["published"],"metadata_version":"2.0","created":"2026-05-24","updated":"2026-07-10 14:30:00","directory":"03_Output/Articles","title":"Obsidian新手入门：花10分钟搭建一个最简单实用的Dashboard","summary":"dataview插件：dataviewjs实现可视化","tags":["Dashboard","入门教程","插件"],"area":"知识管理","word_count":0,"reading_time":0,"publish_status":"draft","publish_date":"2026-06-10","primary_platform":"微信公众号","publish_platforms":null,"publish_url":"","views":798,"likes":11,"comments":0,"collections":28,"progress":0,"archived":false,"related_notes":["[[03_Output/Articles/小红书版_Obsidian新手入门：花10分钟搭建一个最简单实用的Dashboard/小红书版_Obsidian新手入门：花10分钟搭建一个最简单实用的Dashboard]]"],"related_products":[],"shares":88,"avg_read_time":0.55,"completion_rate":0.15,"readers":806,"new_user":10}}
---

# 标题：Obsidian新手入门：花10分钟搭建一个最简单实用的Dashboard

在优化我自己的全球订阅输入系统的时候，一直纠结要不要打磨一个完美的Dashboard。但是，我又不想去过度的研究CSS，因为，过去的折腾经验告诉我，不太过度去打磨美观，应该更专注到内容本身。

但是，为了可以更清晰更方便的量化监控输入系统的状态和情况，建立一个基础的简易可行的Dashboard还是有必要的。

因为有了Dashboard，既可以汇总核心监控数据，又可以浏览起来相对美观，只是不要花太多时间去打磨排版和配色。这是我经过几年折腾后，当前深度使用obsidian的唯一原则。

下面就来尝试通过10分钟，搭建一个最简单实用的Dashboard。原则如下：

1. 不过度调整配色和排版
2. 不依赖使用CSS来设计排版
3. 不过度使用太多插件
4. 依赖AI进行基础代码赋能

## 第一栏：原则

做任何事情都要记住自己的原则和底线，因此，我第一行放了一个自己的原则引用：
![03_Output/Articles/Obsidian新手入门：花10分钟搭建一个最简单实用的Dashboard/插图1.png](/img/user/03_Output/Articles/Obsidian%E6%96%B0%E6%89%8B%E5%85%A5%E9%97%A8%EF%BC%9A%E8%8A%B110%E5%88%86%E9%92%9F%E6%90%AD%E5%BB%BA%E4%B8%80%E4%B8%AA%E6%9C%80%E7%AE%80%E5%8D%95%E5%AE%9E%E7%94%A8%E7%9A%84Dashboard/%E6%8F%92%E5%9B%BE1.png)

任何事情急不来，只有有了更优质的输入，才能慢慢的提高输出的质量，因此，大家可以结合自己的原则在第一行放入自己的习惯和心态，作为一个提醒。

## 第二栏：卡片导航

如果是专门用来统计输入的情况，可以建立几个核心卡片，来统计：
* 今日输入
* 本周输入
* 本月输入
* 总输入数

![03_Output/Articles/Obsidian新手入门：花10分钟搭建一个最简单实用的Dashboard/插图2.png](/img/user/03_Output/Articles/Obsidian%E6%96%B0%E6%89%8B%E5%85%A5%E9%97%A8%EF%BC%9A%E8%8A%B110%E5%88%86%E9%92%9F%E6%90%AD%E5%BB%BA%E4%B8%80%E4%B8%AA%E6%9C%80%E7%AE%80%E5%8D%95%E5%AE%9E%E7%94%A8%E7%9A%84Dashboard/%E6%8F%92%E5%9B%BE2.png)

以上作为一个参考，每个人的不同领域，可以监控不同的核心指标，方便每日浏览一下。比如：英语词汇，输出总数等。

重点是如何制作这个卡片，以上卡片不需要css辅助排版，只需要通过dataviewjs融入自动获取属性字段和少量卡片代码即可。

```
```dataviewjs
const inputPages = dv.pages("#输入");

const total = inputPages.length;

const today = window.moment().format("yyyy-MM-dd");
const currentWeek = window.moment().week();
const currentMonth = window.moment().format("yyyy-MM");

const todayCount = inputPages.where(p =>
    p.file.cday.toFormat("yyyy-MM-dd") === today
).length;

const weekCount = inputPages.where(p =>
    window.moment(p.file.cday.toString()).week() === currentWeek
).length;

const monthCount = inputPages.where(p =>
    p.file.cday.toFormat("yyyy-MM") === currentMonth
).length;


/* 创建整体容器 */
const container = document.createElement("div");

container.style.cssText = `
    display:grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap:16px;
    width:100%;
`;


/* 创建卡片函数 */
function createCard(icon, number, title) {

    const card = document.createElement("div");

    card.style.cssText = `
        background:#f5f3ef;
        border-radius:28px;
        padding:28px;
        min-height:220px;

        display:flex;
        flex-direction:column;
        justify-content:space-between;

        box-shadow:0 4px 20px rgba(0,0,0,0.04);

        overflow:hidden;
    `;

    card.innerHTML = `
        <div style="
            font-size:42px;
        ">
            ${icon}
        </div>

        <div>
            <div style="
                font-size:62px;
                font-weight:700;
                line-height:1;
                color:#334964;
                margin-bottom:10px;
            ">
                ${number}
            </div>

            <div style="
                font-size:18px;
                color:#5b6777;
                font-weight:600;
            ">
                ${title}
            </div>
        </div>
    `;

    container.appendChild(card);
}


/* 添加4个卡片 */
createCard("📥", todayCount, "今日输入");
createCard("📅", weekCount, "本周输入");
createCard("🗂️", monthCount, "本月输入");
createCard("📚", total, "总输入数");


/* 渲染 */
dv.container.appendChild(container);
```

以上代码并不需要自己去专研，只要提出需求让Deepseek直接提供代码即可。属性字段需要自己建立笔记字段，比如：全球订阅输入系统有固定的笔记存储模版，当你每日自动存储后，dashboard就会按照对应字段自动统计渲染展示。

## 第三栏：分栏数据

一个完整的dashboard除了卡片指标，还可能有趋势图，表格、明细等等数据，因此，在不需要太美观的基础上，要想快速实现，就可以通过Multi-Markdown分栏插件来快速实现。

整体代码非常简单，快捷键Command+P，选择Multi-Markdown插入分栏功能，代码如下：
![03_Output/Articles/Obsidian新手入门：花10分钟搭建一个最简单实用的Dashboard/插图3.png\|467](/img/user/03_Output/Articles/Obsidian%E6%96%B0%E6%89%8B%E5%85%A5%E9%97%A8%EF%BC%9A%E8%8A%B110%E5%88%86%E9%92%9F%E6%90%AD%E5%BB%BA%E4%B8%80%E4%B8%AA%E6%9C%80%E7%AE%80%E5%8D%95%E5%AE%9E%E7%94%A8%E7%9A%84Dashboard/%E6%8F%92%E5%9B%BE3.png)

渲染如下：

![03_Output/Articles/Obsidian新手入门：花10分钟搭建一个最简单实用的Dashboard/插图4.png](/img/user/03_Output/Articles/Obsidian%E6%96%B0%E6%89%8B%E5%85%A5%E9%97%A8%EF%BC%9A%E8%8A%B110%E5%88%86%E9%92%9F%E6%90%AD%E5%BB%BA%E4%B8%80%E4%B8%AA%E6%9C%80%E7%AE%80%E5%8D%95%E5%AE%9E%E7%94%A8%E7%9A%84Dashboard/%E6%8F%92%E5%9B%BE4.png)

对于详细的Multi-Markdown插件使用方法历史分享过，不再赘述。下面是分两栏来监控输入详情和输入数量。

![03_Output/Articles/Obsidian新手入门：花10分钟搭建一个最简单实用的Dashboard/插图5.png](/img/user/03_Output/Articles/Obsidian%E6%96%B0%E6%89%8B%E5%85%A5%E9%97%A8%EF%BC%9A%E8%8A%B110%E5%88%86%E9%92%9F%E6%90%AD%E5%BB%BA%E4%B8%80%E4%B8%AA%E6%9C%80%E7%AE%80%E5%8D%95%E5%AE%9E%E7%94%A8%E7%9A%84Dashboard/%E6%8F%92%E5%9B%BE5.png)

## 第四栏：习惯监控

很多时候，最影响我们的是无法坚持学习或者输入，因此，通过一个热力图直观的看到自己的坚持状态和质量，是非常有必要的，也是可以帮助我们坚持的一个数据。

因此，通过一个简单的热力图Heatmap Calendar插件即可实现，非常简单：

![03_Output/Articles/Obsidian新手入门：花10分钟搭建一个最简单实用的Dashboard/插图6.png](/img/user/03_Output/Articles/Obsidian%E6%96%B0%E6%89%8B%E5%85%A5%E9%97%A8%EF%BC%9A%E8%8A%B110%E5%88%86%E9%92%9F%E6%90%AD%E5%BB%BA%E4%B8%80%E4%B8%AA%E6%9C%80%E7%AE%80%E5%8D%95%E5%AE%9E%E7%94%A8%E7%9A%84Dashboard/%E6%8F%92%E5%9B%BE6.png)

## 第五栏：数据补充和收尾

最后可以再补充一些需要量化监控的数据或者明细，同时也可以有一个简单的dashboard收尾。
![03_Output/Articles/Obsidian新手入门：花10分钟搭建一个最简单实用的Dashboard/插图7.png](/img/user/03_Output/Articles/Obsidian%E6%96%B0%E6%89%8B%E5%85%A5%E9%97%A8%EF%BC%9A%E8%8A%B110%E5%88%86%E9%92%9F%E6%90%AD%E5%BB%BA%E4%B8%80%E4%B8%AA%E6%9C%80%E7%AE%80%E5%8D%95%E5%AE%9E%E7%94%A8%E7%9A%84Dashboard/%E6%8F%92%E5%9B%BE7.png)

通过最后一栏给自己一句话，长期主义比爆发更重要，可以每次提醒自己，一定要坚持长期主义深耕，才是最稳妥有效的成长道路。

## 总结

通过最简单的插件和AI的代码协助，并不需要太久，就可以组合一个最简单实用，且相对美观浏览的dashboard。给自己的不同领域都可以尝试去又一个数据监控，才能更清晰的量化推动自己的脚步。

![03_Output/Articles/Obsidian新手入门：花10分钟搭建一个最简单实用的Dashboard/插图8.png](/img/user/03_Output/Articles/Obsidian%E6%96%B0%E6%89%8B%E5%85%A5%E9%97%A8%EF%BC%9A%E8%8A%B110%E5%88%86%E9%92%9F%E6%90%AD%E5%BB%BA%E4%B8%80%E4%B8%AA%E6%9C%80%E7%AE%80%E5%8D%95%E5%AE%9E%E7%94%A8%E7%9A%84Dashboard/%E6%8F%92%E5%9B%BE8.png)
![03_Output/Articles/Obsidian新手入门：花10分钟搭建一个最简单实用的Dashboard/插图9.png](/img/user/03_Output/Articles/Obsidian%E6%96%B0%E6%89%8B%E5%85%A5%E9%97%A8%EF%BC%9A%E8%8A%B110%E5%88%86%E9%92%9F%E6%90%AD%E5%BB%BA%E4%B8%80%E4%B8%AA%E6%9C%80%E7%AE%80%E5%8D%95%E5%AE%9E%E7%94%A8%E7%9A%84Dashboard/%E6%8F%92%E5%9B%BE9.png)

希望大家都可以用最简单的方式搭建自己的dashboard或者系统，专注到自己的输入系统和输入中。

