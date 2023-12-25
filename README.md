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
