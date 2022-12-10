# logseq-developer-theme

[![build and deploy](https://img.shields.io/github/workflow/status/UNICKCHENG/logseq-developer-theme/build%20and%20deploy/main?label=build)](https://github.com/UNICKCHENG/logseq-developer-theme/actions/workflows/build-and-deploy.yml)
[![logseq](https://img.shields.io/github/v/release/UNICKCHENG/logseq-developer-theme)](https://github.com/UNICKCHENG/logseq-developer-theme/releases)
[![logseq-dev-theme](https://img.shields.io/github/workflow/status/pengx17/logseq-dev-theme/Deploy/main?label=logseq-dev-theme)](https://github.com/pengx17/logseq-dev-theme/actions/workflows/main.yml)
[![logseq](https://img.shields.io/github/v/release/logseq/logseq?label=logseq)](https://github.com/logseq/logseq/releases)

[中文版](readme-zh.md)

[logseq-developer-theme](https://github.com/UNICKCHENG/logseq-developer-theme) is a secondary development of the [logseq-dev-theme](https://github.com/pengx17/logseq-dev-theme) theme as an upstream, and you can easily see the `@import` reference in [main.scss](scss/main.scss) . You can clearly compare the differences between [logseq-dev-theme](https://pengx17.github.io/knowledge-garden/) and [logseq-developer-theme](https://docs.unickcheng.cc/#/page/%E5%B9%B3%E5%8F%B0%E9%A3%9F%E7%94%A8%E6%8C%87%E5%8C%97) via respective website, for more information see [this article](https://docs.unickcheng.cc/#/page/logseq-developer-theme).

**logseq-developer-theme will not be made into logseq-dev-theme 2.0**, just because logseq-dev-theme allows me to focus more on the desired css style, therefore, this project is not a fork, but a reference via `@import`.

For the record, I don't have any experience in front-end development, but the best method to start learning is with a project. Although [scss](https://sass-lang.com/documentation/syntax) is not very complicated, the code I wrote was really ugly. So I will keep improving the code and you can also remind me at [issues](https://github.com/UNICKCHENG/logseq-developer-theme/issues) or pull request. 


## 🎉Usage

Using the jsDelivr CDN to get theme styles , simply add the following code to your `custom.css`. 

```css
@import url("https://cdn.jsdelivr.net/gh/unickcheng/developer-theme-for-logseq@release/custom.css");
```
⚠️ Please note that the jsDelivr CDN provides a faster service, but may not be able to refresh the latest version in time [^1]

![](assets/Pasted%20image%2020221210174733.png)

![](assets/Pasted%20image%2020221210174750.png)

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

[^1]: https://blog.juanertu.com/archives/cbcd1946
