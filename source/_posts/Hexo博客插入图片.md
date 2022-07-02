---
title: Hexo博客插入图片
date: 2022-07-01 15:29:28
tags:
---
## 前言
在md文件中插入图片的语法为 `![]()` 。其中方括号是图片描述，圆括是图片路径。我们的图片路径使用相对路径。

在hexo中使用文章资源文件夹需要在 `_config.yaml` 文件中更改一下配置：
```
post_asset_folder: true
```
当该配置被应用后，使用 `hexo new` 命令创建新文章md文件时，会生成相同名字的文件夹，也就是文章资源文件夹。也可以直接新建md文件和同名的文件夹，效果是一样的。

在新文章md文件中插入图片，图片存放的位置是和新文章md文件同名的文件夹；图片的路径不太好写，这是需要借助插件。

## hexo-asset-image-for-hexo5插件
[hexo-asset-image-for-hexo5](https://github.com/uinika/hexo-asset-image-for-hexo5)

安装这个插件之后，图片的路径直接使用图片的文件名即可。
```bash
├─Data-Structure
├── logo.jpg
└─Data-Structure.md
```
使用 `![logo](Data-Structure/logo.jpg)` 来插入图片。

## 注意
建议使用Typora工具书写md文件

可以使用python脚本去除文件夹中多余的图片

在Typora中可以使用在图片后面敲空格使得图片左对齐，但是推送到网站上就不能左对齐了

<img src="Hexo博客插入图片/01.jpg" alt="01" style="zoom:25%;" /> 
