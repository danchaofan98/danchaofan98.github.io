---
title: Hexo博客插入图片
date: 2022-07-01 15:29:28
tags:
---
## 前言
在md文件中插入图片的语法为`![]()`。其中方括号是图片描述，圆括是图片路径。我们的图片路径使用相对路径。

在hexo中使用文章资源文件夹需要在`_config.yaml`文件中更改一下配置：
```
post_asset_folder: true
```
当该配置被应用后，使用`hexo new`命令创建新文章md文件时，会生成相同名字的文件夹，也就是文章资源文件夹。

在新文章md文件中插入图片，图片存放的位置是和新文章md文件同名的文件夹；图片的路径不太好写，这是需要借助插件。

## hexo-asset-image插件
[hexo-asset-image插件](https://github.com/xcodebuild/hexo-asset-image)

安装这个插件之后，图片的路径直接使用图片的文件名即可。
```
MacGesture2-Publish
├── apppicker.jpg
├── logo.jpg
└── rules.jpg
MacGesture2-Publish.md
```
使用`![logo](logo.jpg)`来插入图片。

## 注意
使用VSCode写md文件，对于图片的处理，使用Markdown Image扩展，将图片默认存储路径中的images删掉，这样图片就保存在和md文件同级目录下，插入图片时，图片的路径就自然是图片的文件名。写完之后再将所有图片移动到新文章md文件夹。


