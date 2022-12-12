# logseq-developer-theme

[![Release](https://github.com/UNICKCHENG/logseq-developer-theme/actions/workflows/release.yml/badge.svg)](https://github.com/UNICKCHENG/logseq-developer-theme/actions/workflows/release.yml)
[![release](https://img.shields.io/github/v/release/UNICKCHENG/logseq-developer-theme)](https://github.com/UNICKCHENG/logseq-developer-theme/releases)
[![logseq-dev-theme](https://img.shields.io/github/workflow/status/pengx17/logseq-dev-theme/Deploy/main?label=logseq-dev-theme)](https://github.com/pengx17/logseq-dev-theme/actions/workflows/main.yml)
[![logseq](https://img.shields.io/github/v/release/logseq/logseq?label=logseq)](https://github.com/logseq/logseq/releases)

[中文版](readme-zh.md)

[logseq-developer-theme](https://github.com/UNICKCHENG/logseq-developer-theme) is a secondary development of the [logseq-dev-theme](https://github.com/pengx17/logseq-dev-theme) theme as an upstream, and you can easily see the `@import` reference in [main.scss](scss/main.scss) . You can clearly compare the differences between [logseq-dev-theme](https://pengx17.github.io/knowledge-garden/) and [logseq-developer-theme](https://docs.unickcheng.cc) via respective website [^1] [^2], for more information see [this article](https://docs.unickcheng.cc/#/page/logseq-developer-theme).

**logseq-developer-theme will not be made into logseq-dev-theme 2.0**, just because logseq-dev-theme allows me to focus more on the desired css style, therefore, this project is not a fork, but a reference via `@import`.

For the record, I don't have any experience in front-end development, but the best method to start learning is with a project. Although [scss](https://sass-lang.com/documentation/syntax) is not very complicated, the code I wrote was really ugly. So I will keep improving the code and you can also remind me at [issues](https://github.com/UNICKCHENG/logseq-developer-theme/issues) or pull request. 

## ✨Features

- [X] enhance code block style , especially color
- [X] support tag some tags highlighting
- [X] adapt Chinese font style
- [X] support user-defined theme colors
- [ ] support download in plugin marketplace
- [ ] supports use in offline mode

## 🎉Usage

Using the jsDelivr CDN to get theme styles , simply add the following code to your `custom.css`. 

```css
@import url("https://cdn.jsdelivr.net/gh/unickcheng/logseq-developer-theme@release/custom.css")
```
⚠️ Please note that the jsDelivr CDN provides a faster service, but may not be able to refresh the latest version in time [^3]

![](assets/Pasted%20image%2020221210174733.png)

![](assets/Pasted%20image%2020221210174750.png)

Starting with version 0.4.0, you can also customize the theme colors 😎 

```css
@import url("https://cdn.jsdelivr.net/gh/unickcheng/logseq-developer-theme@release/custom.css")
.dark-theme,
html[data-theme=dark] {
    --ls-primary-background-color: #272C35;
    --ls-secondary-background-color: #313942;

    --ls-primary-theme-color: #fff;
    --ls-secondary-theme-color: #6096BA;
    --ls-third-theme-color: gray;

    --ls-code-color: #fff;
    --ls-code-background-color: #34343c;
    --ls-code-selected-background-color: #32445A;
}
```
![](assets/Pasted%20image%2020221212235959.png)

```css
@import url("https://cdn.jsdelivr.net/gh/unickcheng/logseq-developer-theme@release/custom.css")
.white-theme,
html[data-theme=light] {
    --ls-primary-background-color: #ffC017;
    --ls-secondary-background-color: #ffcf4d;
    
    --ls-primary-theme-color: #000;
    --ls-secondary-theme-color: rgb(224, 80, 27);
    --ls-third-theme-color: gray;

    --ls-code-color: gray;
    --ls-code-background-color: #fff ;
    --ls-code-selected-background-color: #C0E6FD;
}
```
![](assets/Pasted%20image%2020221213001146.png)

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
