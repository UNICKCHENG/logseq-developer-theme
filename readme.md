# logseq-developer-theme

[![Release](https://github.com/UNICKCHENG/logseq-developer-theme/actions/workflows/release.yml/badge.svg)](https://github.com/UNICKCHENG/logseq-developer-theme/actions/workflows/release.yml)
[![release](https://img.shields.io/github/v/release/UNICKCHENG/logseq-developer-theme)](https://github.com/UNICKCHENG/logseq-developer-theme/releases)
[![logseq-dev-theme](https://img.shields.io/github/v/release/pengx17/logseq-dev-theme?label=logseq-dev-theme)](https://github.com/pengx17/logseq-dev-theme/actions/workflows/main.yml)
[![logseq](https://img.shields.io/github/v/release/logseq/logseq?label=logseq)](https://github.com/logseq/logseq/releases)

[中文版](readme-zh.md)

[logseq-developer-theme](https://github.com/UNICKCHENG/logseq-developer-theme) is a secondary development of the [logseq-dev-theme](https://github.com/pengx17/logseq-dev-theme) theme as an upstream, and you can easily see the `@import` reference in [main.scss](scss/main.scss) . You can clearly compare the differences between [logseq-dev-theme](https://pengx17.github.io/knowledge-garden/) and [logseq-developer-theme](https://docs.unickcheng.cc) via respective website [^1] [^2], for more information see [this article](https://docs.unickcheng.cc/#/page/logseq-developer-theme).

**logseq-developer-theme will not be made into logseq-dev-theme 2.0**, just because logseq-dev-theme allows me to focus more on the desired css style, therefore, this project is not a fork, but a reference via `@import`.

For the record, I don't have any experience in front-end development, but the best method to start learning is with a project. Although [scss](https://sass-lang.com/documentation/syntax) is not very complicated, the code I wrote was really ugly. So I will keep improving the code and you can also remind me at [issues](https://github.com/UNICKCHENG/logseq-developer-theme/issues) or pull request. 

<a href="https://www.buymeacoffee.com/unickcheng"><img src="https://img.buymeacoffee.com/button-api/?text=Buy me a tea&emoji=&slug=unickcheng&button_colour=FFDD00&font_colour=000000&font_family=Cookie&outline_colour=000000&coffee_colour=ffffff" /></a>

## ✨Features

- [x] enhance code block style , especially color
- [X] support some tags highlighting， such as `#docs`, `#bug`, `#feat`, etc
- [X] adapt Chinese font style
- [X] support user-defined theme colors
- [X] support download in plugin marketplace [#297](https://github.com/logseq/marketplace/pull/297)
- [X] supports use in offline mode
- [X] supports custom pdf color 

## 🎉Usage

### Quick Start

Using the jsDelivr CDN to get theme styles , simply add the following code to your `custom.css`. 

```css
@import url("https://cdn.jsdelivr.net/gh/unickcheng/logseq-developer-theme@release/custom.css");
```
⚠️ Please note that the jsDelivr CDN provides a faster service, but may not be able to refresh the latest version in time [^3]

###  Download from Plugin Marketplace（Recommend）

![](assets/Pasted%20image%2020221216222925.png)

If you can't download it from the plugin marketplace, you can download it from  [GitHub Release](https://github.com/UNICKCHENG/logseq-developer-theme/releases) , unzip it, and then import it into logseq

![](assets/Pasted%20image%2020221216223400.png)
![](assets/Pasted%20image%2020221216223545.png)

📌 Starting with version 1.0.0, GitHub Release or Plugin Marketplace downloads are supported for offline use. Because it will download fonts and other dependencies together to the local `~/.logseq/plugins` directory.

## Demo(may be outdated)

![](assets/Pasted%20image%2020221210174733.png)

![](assets/Pasted%20image%2020221210174750.png)

![](assets/Pasted%20image%2020221216232448.png)

Starting with version 0.4.0, you can also customize the theme colors 😎 

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

> For more custom colors see  [custom-color](custom-color.md)

## 🚀 Local development

**step 1 > Verify the local environment**
```bash
node -v
npm -v
git -v
```

**step 2 > Install dependencies**
```bash
# > step 1 download source code
git clone https://github.com/UNICKCHENG/logseq-developer-theme.git
cd logseq-developer-theme
# > step 2 installing dependencies
npm install
```

**step 3 > Modify  `package.json`**
- please modify value of `localPath` to the address of your logseq graph documentation
```
{
	...
    "config": {
        "localPath": "C:\\Users\\hi\\LocalStation\\BLOG\\docs"
    },
	...
}
```
⚠️ The purpose here is to make it easier to compile the SCSS output directly to `../logseq/custom.css`

**step 4 > Running**
```bash
# windows
npm run dev:win

# Mac or Linux
npm run dev
```

## ✍️Changelog

You can see more information at [logseq-developer-theme](https://docs.unickcheng.cc/#/page/logseq-developer-theme)

## 💖 Credits

- [logseq team](https://github.com/logseq/logseq)
- [pengx17/logseq-dev-theme](https://github.com/pengx17/logseq-dev-theme)
- [flowerornament/logseq-simple-parametric-theme](https://github.com/flowerornament/logseq-simple-parametric-theme) for code block CSS Style
- [ryanoasis/nerd-fonts](https://github.com/ryanoasis/nerd-fonts) support about DejaVuSansMono Fonts
- [lxgw/LxgwWenKai-Lite](https://github.com/lxgw/LxgwWenKai-Lite) support about LXGWWenKaiLite-Regular Fonts
- [awesome-logseq](https://github.com/logseq/awesome-logseq) provides list of logeseq theme
- [RemNote](https://github.com/orgs/remnoteio/repositories) default theme style
- Thanks to all open source projects for sharing ideas and techniques

[^1]: https://pengx17.github.io/knowledge-garden/
[^2]: https://docs.unickcheng.cc
[^3]: https://blog.juanertu.com/archives/cbcd1946
