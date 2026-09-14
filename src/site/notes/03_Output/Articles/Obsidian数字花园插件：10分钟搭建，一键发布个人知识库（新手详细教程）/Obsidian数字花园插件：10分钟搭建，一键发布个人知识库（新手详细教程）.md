---
{"dg-publish":true,"permalink":"/03-output/articles/obsidian-10/obsidian-10/","title":"Obsidian数字花园插件：10分钟搭建，一键发布个人知识库（新手详细教程）","tags":["插件","DigitalGardenWeb"],"dg-note-properties":{"object":"Article","object_cn":"文章","object_abbr":"ART","category":"Content","category_cn":"内容输出","status":["reviewing"],"metadata_version":"2.0","created":"2026-09-04","updated":"2026-09-04","directory":"03_Output/Articles","title":"Obsidian数字花园插件：10分钟搭建，一键发布个人知识库（新手详细教程）","summary":"","tags":["插件","DigitalGardenWeb"],"area":"知识管理","word_count":0,"reading_time":0,"publish_status":"draft","publish_date":null,"primary_platform":"微信公众号","publish_platforms":[],"publish_url":"","views":0,"likes":0,"comments":0,"collections":0,"progress":0,"archived":false,"related_notes":[],"related_products":[],"new_user":0,"readers":0,"shares":0,"avg_read_time":0,"completion_rate":0,"sort_index":19250}}
---

# 标题：Obsidian打造数字花园插件，新手详细教程，实现无忧一键发布


在开始搭建自己的数字花园之前，有几个必备的准备，就是：

1. 下载安装插件
2. 创建数字花园站点
3. 插件配置
4. 测试发布

## 下载安装

在Obsidian设置里面，左侧找到第三方插件，从插件市场搜索：Digital Garden，点击下载安装启用。
![Obsidian插件：Digital Garden-10.png\|423](/img/user/03_Output/Articles/Obsidian%E6%95%B0%E5%AD%97%E8%8A%B1%E5%9B%AD%E6%8F%92%E4%BB%B6%EF%BC%9A10%E5%88%86%E9%92%9F%E6%90%AD%E5%BB%BA%EF%BC%8C%E4%B8%80%E9%94%AE%E5%8F%91%E5%B8%83%E4%B8%AA%E4%BA%BA%E7%9F%A5%E8%AF%86%E5%BA%93%EF%BC%88%E6%96%B0%E6%89%8B%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B%EF%BC%89/Obsidian%E6%8F%92%E4%BB%B6%EF%BC%9ADigital%20Garden-10.png)


## 创建数字花园站点

### 创建仓库

1. 访问 Digital Garden 的模板仓库：[https://github.com/oleeskild/digitalgarden](https://github.com/oleeskild/digitalgarden)
2. 点击绿色的 **“Use this template”** 按钮，然后选择 **“Create a new repository”** 。
3. **重要**：仓库名称必须严格按照格式 `你的GitHub用户名.github.io` 来填写（例如，如果你的用户名是 `foxblock`，仓库名就填 `foxblock.github.io`），并且建议将仓库设为 **公开（Public）**（提醒：如果不按照这个原则命名，后续笔记图片展示会异常，个人亲测踩坑，务必重视）
4. 创建完成后，进入该仓库的 `Settings > Pages`，在 “Build and deployment” 下拉菜单中，选择 `GitHub Actions` ，方便后续自定义自己的首页。

提醒：由于原数字花园官网模版代码中有一处错误会导致部署报错，找到skills文件删除即可。

![Obsidian插件：Digital Garden-8.png](/img/user/03_Output/Articles/Obsidian%E6%95%B0%E5%AD%97%E8%8A%B1%E5%9B%AD%E6%8F%92%E4%BB%B6%EF%BC%9A10%E5%88%86%E9%92%9F%E6%90%AD%E5%BB%BA%EF%BC%8C%E4%B8%80%E9%94%AE%E5%8F%91%E5%B8%83%E4%B8%AA%E4%BA%BA%E7%9F%A5%E8%AF%86%E5%BA%93%EF%BC%88%E6%96%B0%E6%89%8B%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B%EF%BC%89/Obsidian%E6%8F%92%E4%BB%B6%EF%BC%9ADigital%20Garden-8.png)


创建成功后，网站网页初始页面如下：

![Obsidian插件：Digital Garden-9.png](/img/user/03_Output/Articles/Obsidian%E6%95%B0%E5%AD%97%E8%8A%B1%E5%9B%AD%E6%8F%92%E4%BB%B6%EF%BC%9A10%E5%88%86%E9%92%9F%E6%90%AD%E5%BB%BA%EF%BC%8C%E4%B8%80%E9%94%AE%E5%8F%91%E5%B8%83%E4%B8%AA%E4%BA%BA%E7%9F%A5%E8%AF%86%E5%BA%93%EF%BC%88%E6%96%B0%E6%89%8B%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B%EF%BC%89/Obsidian%E6%8F%92%E4%BB%B6%EF%BC%9ADigital%20Garden-9.png)

可以通过https://你的GitHub用户名.github.io来访问测试确认。以上只是当前首页，待进一步发布笔记首页后，进行测试校验。

### 创建令牌

由于在稍后的插件配置里面，需要Github访问令牌，也就是生成一个访问秘钥。因此，需要在新建的仓库来创造。

这个令牌（Token）相当于一把钥匙，Digital Garden 插件需要用它来获得向你的 GitHub 仓库写入笔记的权限。

1. 登录 GitHub，点击右上角头像，进入 **Settings**。
2. 在左侧菜单栏最下方，找到并点击 **Developer settings**。
3. 在左侧菜单中，点击 **Personal access tokens**，然后选择 **Tokens (classic)**。
4. 点击 **Generate new token**，然后选择 **Generate new token (classic)** 
5. 为这个令牌起一个你记得住的名字，比如 `Obsidian Digital Garden`。
6. 在 **Expiration** 下拉菜单中，为了省去频繁更新的麻烦，可以选择 **No expiration**（无有效期）
7. 在 **Scopes**（权限范围）区域，勾选 **repo** 权限，这将赋予插件管理你仓库内容的全部权限。
8. 滚动到页面底部，点击 **Generate token**。
9. **立刻复制并保存好生成的令牌字符串**！这个页面关闭后就再也看不到了。

由于我是在Github app端创建，找不到**Developer settings**，因此，可以通过：**[https://github.com/settings/personal-access-tokens](https://github.com/settings/personal-access-tokens)**，进入如下：

![03_Output/Articles/Obsidian数字花园插件：10分钟搭建，一键发布个人知识库（新手详细教程）/Obsidian插件：Digital Garden.png](/img/user/03_Output/Articles/Obsidian%E6%95%B0%E5%AD%97%E8%8A%B1%E5%9B%AD%E6%8F%92%E4%BB%B6%EF%BC%9A10%E5%88%86%E9%92%9F%E6%90%AD%E5%BB%BA%EF%BC%8C%E4%B8%80%E9%94%AE%E5%8F%91%E5%B8%83%E4%B8%AA%E4%BA%BA%E7%9F%A5%E8%AF%86%E5%BA%93%EF%BC%88%E6%96%B0%E6%89%8B%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B%EF%BC%89/Obsidian%E6%8F%92%E4%BB%B6%EF%BC%9ADigital%20Garden.png)

然后，再按照上述的流程去建立一个token秘钥，保存好后面插件配置使用即可。

## Digital Garden插件配置

点击Obsidian设置里面，找到插件，点击打开插件配置界面，可以看到发布平台默认是Github，不用修改，只需要配置填写以下3个地方：

* GitHub repo name：你的GitHub用户名.github.io
* GitHub Username：用户名
* GitHub token：新创建的秘钥

![Obsidian插件：Digital Garden 1.png](/img/user/03_Output/Articles/Obsidian%E6%95%B0%E5%AD%97%E8%8A%B1%E5%9B%AD%E6%8F%92%E4%BB%B6%EF%BC%9A10%E5%88%86%E9%92%9F%E6%90%AD%E5%BB%BA%EF%BC%8C%E4%B8%80%E9%94%AE%E5%8F%91%E5%B8%83%E4%B8%AA%E4%BA%BA%E7%9F%A5%E8%AF%86%E5%BA%93%EF%BC%88%E6%96%B0%E6%89%8B%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B%EF%BC%89/Obsidian%E6%8F%92%E4%BB%B6%EF%BC%9ADigital%20Garden%201.png)

填写三个参数后，插件会自动校验，如果显示：Connected with full access，证明配置成功。

提醒：base url也需要填上：https://xihutaijixiong.github.io，方便后续保存和图片路径正常。

## build修改

在github中的路径：.github/workflows找到build.yml文件，修改代码如下，可以让后续的首页按照obsidian的设定来渲染展示。

```
name: Build and Deploy Digital Garden

on:
  push:
    branches: ["main"]
  pull_request:
    branches: ["main"]
  workflow_dispatch:

permissions:
  contents: read
  pages: write
  id-token: write

jobs:
  build:
    runs-on: ubuntu-24.04

    steps:
      - name: Checkout
        uses: actions/checkout@v6

      - name: Setup Node.js
        uses: actions/setup-node@v7
        with:
          node-version: 24
          cache: npm

      - name: Install dependencies
        run: npm ci

      - name: Build Digital Garden
        run: npm run build

      - name: Setup GitHub Pages
        if: github.event_name == 'push' || github.event_name == 'workflow_dispatch'
        uses: actions/configure-pages@v5

      - name: Upload Pages artifact
        if: github.event_name == 'push' || github.event_name == 'workflow_dispatch'
        uses: actions/upload-pages-artifact@v4
        with:
          path: ./dist

  deploy:
    if: github.event_name == 'push' || github.event_name == 'workflow_dispatch'
    needs: build

    runs-on: ubuntu-24.04

    environment:
      name: github-pages
      url: ${{ steps.deployment.outputs.page_url }}

    steps:
      - name: Deploy to GitHub Pages
        id: deployment
        uses: actions/deploy-pages@v4
```

## 发布设置

对于发布最重要的就是两个属性：

发布首页：
```
---
dg-home: true
dg-publish: true
---
```
发布非首页
```
---
dg-publish: true
---
```

### 测试笔记发布

通过command+p，可以看到发布快捷选项：Digital Garden: Publish Active Note。选中发布即可。然后这个Obsidian笔记页面就发布到Github模版默认的保存文件中。

![Obsidian插件：Digital Garden-11.png](/img/user/03_Output/Articles/Obsidian%E6%95%B0%E5%AD%97%E8%8A%B1%E5%9B%AD%E6%8F%92%E4%BB%B6%EF%BC%9A10%E5%88%86%E9%92%9F%E6%90%AD%E5%BB%BA%EF%BC%8C%E4%B8%80%E9%94%AE%E5%8F%91%E5%B8%83%E4%B8%AA%E4%BA%BA%E7%9F%A5%E8%AF%86%E5%BA%93%EF%BC%88%E6%96%B0%E6%89%8B%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B%EF%BC%89/Obsidian%E6%8F%92%E4%BB%B6%EF%BC%9ADigital%20Garden-11.png)

### 测试Obsidian首页发布

属性添加dg-home: true，然后选择发布，github会自动部署，发布首页必须在发布笔记之后，对应首页的链接才会生效。

![Obsidian插件：Digital Garden-1.png](/img/user/03_Output/Articles/Obsidian%E6%95%B0%E5%AD%97%E8%8A%B1%E5%9B%AD%E6%8F%92%E4%BB%B6%EF%BC%9A10%E5%88%86%E9%92%9F%E6%90%AD%E5%BB%BA%EF%BC%8C%E4%B8%80%E9%94%AE%E5%8F%91%E5%B8%83%E4%B8%AA%E4%BA%BA%E7%9F%A5%E8%AF%86%E5%BA%93%EF%BC%88%E6%96%B0%E6%89%8B%E8%AF%A6%E7%BB%86%E6%95%99%E7%A8%8B%EF%BC%89/Obsidian%E6%8F%92%E4%BB%B6%EF%BC%9ADigital%20Garden-1.png)

## 总结

对于希望建立一个自己的对外可访问的个人知识库，通过Obsidian插件Digital Garden是最方便的，搭建好以后，只要觉得好的点击一下发布即可，如果首页有链接再更新即可。通过这种工作模式，可以不用维护另外一套对应网站的内容库，又进一步all in one到obsidian中。



