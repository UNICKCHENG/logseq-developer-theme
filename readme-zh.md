# logseq-developer-theme

[logseq-developer-theme](https://github.com/UNICKCHENG/logseq-developer-theme)  是将 [logseq-dev-theme](https://github.com/pengx17/logseq-dev-theme) 主题作为上游的二次开发，您可以在 [main.scss](scss/main.scss) 看到 `@import` 引用信息。如果您想知道二者的区别，可以通过各自的网站清楚地比较 [logseq-dev-theme](https://pengx17.github.io/knowledge-garden/)  和 [logseq-developer-theme](https://docs.unickcheng.cc) [^1] [^2]，同时这个项目也在 [这篇文章](https://docs.unickcheng.cc/#/page/logseq-developer-theme)下进行跟进。

**logseq-developer-theme 并不会成为 logseq-dev-theme 2.0**，仅仅因为 logseq-dev-theme 让我更关注于开发期望的 css 样式，因此这个项目不是一个 fork，而是通过 `@import` 来引用它。

声明下，我并没有前端的开发经验，但是最好的学习方法应该从一个项目开始。尽管 [scss](https://sass-lang.com/documentation/syntax) 并不是很复杂，可我写的代码确实很差劲。所以我将持续优化代码，您也可以在 [issues](https://github.com/UNICKCHENG/logseq-developer-theme/issues) 中提醒我，或者参与进来。

<a href="https://www.buymeacoffee.com/unickcheng"><img src="https://img.buymeacoffee.com/button-api/?text=Buy me a tea&emoji=&slug=unickcheng&button_colour=FFDD00&font_colour=000000&font_family=Cookie&outline_colour=000000&coffee_colour=ffffff" /></a>

## ✨Features

- [X] 代码块样式增强，尤其颜色
- [X] 支持部分标签高亮显示，如 `#docs`、`#bug`、`#feat` 等
- [X] 适配中文字体样式
- [X] 支持用户自定义主题颜色
- [X] 支持在插件市场下载 [#297](https://github.com/logseq/marketplace/pull/297)
- [X] 支持离线模式下使用
- [X] 支持自定义 pdf 页面相关颜色

## 🎉使用方法

### 快速开始

您可以借助  jsDelivr CDN 来快速在您的 `custom.css` 中配置

```css
@import url("https://cdn.jsdelivr.net/gh/unickcheng/logseq-developer-theme@release/custom.css");
```
⚠️ 请注意，虽然  jsDelivr CDN 比使用 GitHub 自带的方式更快速，但是它无法做到实时更新到最新版本 [^3]。

###  从插件市场下载（推荐）

![](assets/Pasted%20image%2020221216222925.png)

如果您无法从插件市场下载，可以在 [GitHub Release](https://github.com/UNICKCHENG/logseq-developer-theme/releases) 进行下载，解压后再导入到 logseq

![](assets/Pasted%20image%2020221216223400.png)

![](assets/Pasted%20image%2020221216223545.png)

 📌 从 1.0.0 版本开始，GitHub Release 或者 Plugin Marketplace 下载，支持离线使用。因为会一起将字体等依赖下载到本地 `~/.logseq/plugins` 目录下。

## 效果图 (可能已过时)

![](assets/Pasted%20image%2020221210174733.png)

![](assets/Pasted%20image%2020221210174750.png)

![](assets/Pasted%20image%2020221216232448.png)

从 0.4.0 版本开始，您也可以自定义主题颜色 😎

```css
@import url("https://cdn.jsdelivr.net/gh/unickcheng/logseq-developer-theme@release/custom.css");

.dark-theme,
html[data-theme=dark] {
    --ls-custom-theme-color: #6096BA;
    --ls-primary-background-color: #272C35;
    --ls-secondary-background-color: #313942;

    --ls-code-color: #fff;
    --ls-code-language-color: gray;
    --ls-code-background-color: #34343c;
    --ls-code-selected-background-color: #32445A;

    --ls-bullet-threading-background-color: #34343c;
    --ls-task-done-text-color: gray;
}
```

![](assets/Pasted%20image%2020221216231143.png)

```css
@import url("https://cdn.jsdelivr.net/gh/unickcheng/logseq-developer-theme@release/custom.css");
.white-theme,
html[data-theme=light] {
    --ls-custom-theme-color: rgb(224, 80, 27);
    --ls-primary-background-color: #ffC017;
    --ls-secondary-background-color: #ffcf4d;

    --ls-code-color: gray;
    --ls-code-language-color: gray;
    --ls-code-background-color: #fff;
    --ls-code-selected-background-color: #C0E6FD;

    --ls-bullet-threading-background-color: #ffcf4d;
    --ls-task-done-text-color: gray;
}
```
![](assets/Pasted%20image%2020221216231911.png)

> 更多自定义颜色样式见  [custom-color](custom-color.md)


## 🚀 本地开发

**第一步，验证本地环境**
```bash
node -v
npm -v
git -v
```

**第二步，安装依赖**
```bash
# > step 1 下载源码
git clone https://github.com/UNICKCHENG/logseq-developer-theme.git
cd logseq-developer-theme
# > step 2 安装依赖
npm install
```

**第三步，修改 `package.json` 中的配置**
- 请将 `localPath` 变量值修改为您的文件路径
```
{
	...
    "config": {
        "localPath": "C:\\Users\\hi\\LocalStation\\BLOG\\docs"
    },
	...
}
```
⚠️ 这里的目的是直接将 SCSS 编译后输出到 `../logseq/custom.css`

**第四步，运行**
```bash
# 如果您是 windows 用户
npm run dev:win

# 如果您是 Mac 或者 Linux 用户
npm run dev
```


## ✍️日志

您可以在 [logseq-developer-theme](https://docs.unickcheng.cc/#/page/logseq-developer-theme) 查看相关信息


## 💖 感谢

- [logseq team](https://github.com/logseq/logseq)
- [pengx17/logseq-dev-theme](https://github.com/pengx17/logseq-dev-theme)
- [flowerornament/logseq-simple-parametric-theme](https://github.com/flowerornament/logseq-simple-parametric-theme) 代码块模块样式
- [ryanoasis/nerd-fonts](https://github.com/ryanoasis/nerd-fonts) 关于 DejaVuSansMono 字体支持
- [lxgw/LxgwWenKai-Lite](https://github.com/lxgw/LxgwWenKai-Lite) 关于  LXGWWenKaiLite-Regular 字体支持
- [awesome-logseq](https://github.com/logseq/awesome-logseq) 提供了一份 Logseq 主题清单
- [RemNote](https://github.com/orgs/remnoteio/repositories) 默认主题样式
- 感谢所有开源项目分享的想法和技术


[^1]: https://pengx17.github.io/knowledge-garden/
[^2]: https://docs.unickcheng.cc
[^3]: https://blog.juanertu.com/archives/cbcd1946