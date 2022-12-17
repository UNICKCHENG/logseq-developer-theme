## custom theme

```css
--ls-custom-theme-color: #769AFF;
--ls-primary-background-color: #232329;
--ls-secondary-background-color: #2B2B33;
```

## checkbox

```css
--ls-task-done-text-color: gray;
```


## bullet threading

```css
--ls-bullet-threading-background-color: #34343c;
```

## code block
```css
--ls-code-color: #fff;
--ls-code-language-color: gray;
--ls-code-background-color: #34343c;
--ls-code-selected-background-color: #32445A;
```

## tag

```css
--ls-labels-bug-color: #D46459;
--ls-labels-improvement-color: #4ea7fc;
--ls-labels-feature-color: #BB87FC;
--ls-labels-documentation-color: #0F783C;
--ls-labels-idea-color: #5E6AD2;
--ls-tag-priority-a-color: #000;
--ls-tag-priority-b-color: #000;
--ls-tag-priority-c-color:#000;
--ls-tag-priority-a-background-color: #FF7262;
--ls-tag-priority-b-background-color: #FFC600;
--ls-tag-priority-c-background-color: #E9ECEF;
```

## pdf

```css
--ls-pdf-dark-background-color: #2B2B33;
--ls-pdf-light-background-color: #F7F7F7;
--ls-pdf-warm-background-color: #F9EFDB;

--ls-pdf-dark-selected-background-color: #264F78;
--ls-pdf-light-selected-background-color: #B9E7FF;
--ls-pdf-warm-selected-background-color: #B9E7FF;

--ls-pdf-highlight-red-color: #FCA5A5;
--ls-pdf-highlight-blue-color: #93C5FD;
--ls-pdf-highlight-purple-color: #D884FE;
--ls-pdf-highlight-yellow-color: #FCD34D;
--ls-pdf-highlight-green-color:#86EFAC;
```

## custom fonts

Font selection is not provided, but you can customize the font in the following way

```css
/* --ls-font-family: 正文字体 */
/* --ct-code-font-family: 代码块字体 */
:root {
    --ls-font-family: "Segoe UI", Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji", "Segoe UI Emoji", "Segoe UI Symbol" !important;
    --ct-code-font-family: "Segoe UI", Roboto, Helvetica, Arial, sans-serif !important;
}
```
If you don't really like the default font, but there is no font selection option, i recommend considering the following options
- https://css-tricks.com/snippets/css/system-font-stack/ 
- https://github.com/ryanoasis/nerd-fonts
- https://adobe-fonts.github.io/source-code-pro/
- https://developer.apple.com/fonts/