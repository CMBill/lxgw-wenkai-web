# LXGW WenKai / 霞鹜文楷 网络字体仓库

> 其他版本霞鹜文楷字体的网络字体仓库：
>   - [霞鹜文楷屏幕阅读版 / LXGW WenKai Screen](https://github.com/CMBill/lxgw-wenkai-screen-web)：适用于 PC 和 Android 手机屏幕显示且无需特别切换到粗体。
>   - [霞鹜文楷 GB / LXGW WenKai GB](https://github.com/CMBill/lxgw-wenkai-gb-web)：调整字形和笔形，符合 G 源字形规范。包含《通用规范汉字表》8105 个汉字。
>   - [霞鹜文楷 TC / LXGW WenKai TC](https://github.com/CMBill/lxgw-wenkai-tc-web)：繁体中文版。

## 简介
[LXGW WenKai / 霞鹜文楷](https://github.com/lxgw/LxgwWenKai) 是一款开源中文字体，基于 FONTWORKS 出品字体 Klee One 衍生。字体详情请参阅原字体仓库。

为使原字体更适合进行网络分发，本仓库使用 Github Action，利用[中文网字计划](https://chinese-font.netlify.app/)开发的[字体分包工具](https://github.com/KonghaYao/cn-font-split)对原字体分包，网页加载时只需获取所使用的文字所在的分包，大幅降低所需加载的大小，提升网页加载速度。

为方便使用，本仓库的版本号将与字体原仓库版本号一致。目前只提供了 `v1.315` 及之后的版本。

## 使用
直接将文后提供的链接以 `<link>` 的形式添加到网页的 `<head>` 内即可，这样可以调用上述所有字体及变体，但是只会加载实际使用的字体所在分包文件，如：

```html
<html>
<head>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/CMBill/lxgw-wenkai-web/style.css" />
  <style>
    body {
      font-family: "LXGW WenKai";
      font-weight: normal;
    }
  </style>
</head>
<body>
  
</body>
</html>
```

引入 `style.css` 可以调用仓库包含的如下所有字体，以表格中所示 `font-family` 与 `font-weight` 在 CSS 中调用即可。

| 字体                   | `font-family`            | `font-weight` |
| ---------------------- | ------------------------ | ------------- |
| LXGW Wenkai            | `LXGW Wenkai`            | `normal`      |
| LXGW Wenkai Bold       | `LXGW Wenkai`            | `bold`        |
| LXGW Wenkai Light      | `LXGW Wenkai Light`      | `normal`      |
| LXGW WenKai Mono       | `LXGW WenKai Mono`       | `normal`      |
| LXGW WenKai Mono Bold  | `LXGW WenKai Mono`       | `bold`        |
| LXGW WenKai Mono Light | `LXGW WenKai Mono Light` | `normal`      |

如果只需某一特定的字体，也可只引用其对应分包的 CSS 文件，将如下表格中 `repositoryURL` 替换为仓库的链接即可。

| 字体                   | 链接                                                            |
| ---------------------- | --------------------------------------------------------------- |
| LXGW Wenkai            | `https://repositoryURL/fonts/lxgwwenkai-regular/result.css`     |
| LXGW Wenkai Bold       | `https://repositoryURL/fonts/lxgwwenkai-bold/result.css`        |
| LXGW Wenkai Light      | `https://repositoryURL/fonts/lxgwwenkai-light/result.css`       |
| LXGW WenKai Mono       | `https://repositoryURL/fonts/lxgwwenkaimono-regular/result.css` |
| LXGW WenKai Mono Bold  | `https://repositoryURL/fonts/xgwwenkaimono-bold/result.css`     |
| LXGW WenKai Mono Light | `https://repositoryURL/fonts/lxgwwenkaimono-light/result.css`   |

例如若只需调用 LXGW Wenkai Mono，则只需将链接替换为：
```
https://cdn.jsdelivr.net/gh/CMBill/lxgw-wenkai-web/fonts/lxgwwenkaimono-regular/result.css
``` 

### 自行部署
如果下方提供的链接连接效果不甚理想，建议自行部署并配合自己的 CDN 使用。可以直接 Fork 本仓库并启用 Github Pages，使用时将下方链接修改为自己的仓库地址即可，亦可直接克隆本仓库到服务端、对象存储等。

### 使用 JsDelivr 的 CDN
#### 最新版本
```
https://cdn.jsdelivr.net/gh/CMBill/lxgw-wenkai-web/style.css
```

#### 特定版本 
将链接中的 `$VERSION` 替换为目标版本号，如 `1.315` 或 `v1.315` 均可。目前仅只提供 `v1.315` 之后的版本。
```
https://cdn.jsdelivr.net/gh/CMBill/lxgw-wenkai-web@$VERSION/style.css
```
例如请求 `v1.315` 版本的字体：
```
https://cdn.jsdelivr.net/gh/CMBill/lxgw-wenkai-web@1.315/style.css
```

### 直接使用本仓库链接
只提供最新版本

```
https://cmbill.github.io/lxgw-wenkai-web/style.css
```
