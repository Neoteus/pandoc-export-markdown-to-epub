# Pandoc export MARKDOWN to EPUB

Scripts that call pandoc to export a batch of markdown files to a epub-format book.

调用Pandoc，将多个Markdown转换成Epub格式电子书的脚本。

## Introduction

I was looking for a way to make e-book from markdown, and found a [template](https://github.com/johnpaulada/pandoc-markdown-book-template) for creating epub books from markdown using pandoc. [Pandoc](https://pandoc.org/) is a powerful tool that can convert files from one markup format into another. However, Pandoc does not support fuzzy file names (with wildcard) or directories as input. If there are multiple input files, you need to type each one in the command. So, I write scripts to do this.

I first use Python 3. Then I write batch script to do the same thing. Maybe I will package it and make it more like a complete program in some day, not just script.

## 1. Install Pandoc

You can get Pandoc releases [here](https://github.com/jgm/pandoc/releases).

I also provide direct download links to binary releases below for your convenience, but they may not be the latest version.

### Debian / Ubuntu

[pandoc-2.11.0.4-1-amd64.deb](https://github.com/jgm/pandoc/releases/download/2.11.0.4/pandoc-2.11.0.4-1-amd64.deb)

### Mac OS

Use Homebrew:

    brew install pandoc

or download [pandoc-2.11.0.4-macOS.pkg](https://github.com/jgm/pandoc/releases/download/2.11.0.4/pandoc-2.11.0.4-macOS.pkg)

### Windows x86_64

[pandoc-2.11.0.4-windows-x86_64.msi](https://github.com/jgm/pandoc/releases/download/2.11.0.4/pandoc-2.11.0.4-windows-x86_64.msi)

## 2. Create Book

1. Change to this directory.
2. Replace the content of `title.md` and `images/cover.png` with your own.
3. Write markdown (NO SPACE IN FILE NAME) in `contents` directory, or create directories and subdirectories as you like.
4. Put other images into `images` directory.
5. Run `export-epub.bat` or other script.

Your book will be exported as `book.epub`.

**Note:** If multiple input files are given, pandoc will concatenate them all (with blank lines between them) **in the order of file list** before parsing.

## 简介

我在寻找用markdown制作电子书的方法的过程中，发现了使用pandoc从markdown创建epub书籍的[模板](https://github.com/johnpaulada/pandoc-markdown-book-template)。[Pandoc](https://pandoc.org/)是一个非常强大的文档格式转换工具，但是，Pandoc不支持模糊文件名（带有通配符）或目录作为输入。如果有多个输入文件，则需要在命令中键入每个文件。所以，我写了脚本来做这件事。

我一开始使用Python3。然后我写了批处理脚本(BAT)来实现同样的效果。也许以后我会把它打包，让它更像一个完整的程序，而不仅仅是脚本。

## 1. 安装Pandoc

你可以从[这里](https://github.com/jgm/pandoc/releases)获取Pandoc的发行版。

为了方便，我将二进制版本的下载链接放在下面，但可能不是最新版本：

### Debian / Ubuntu

[pandoc-2.11.0.4-1-amd64.deb](https://github.com/jgm/pandoc/releases/download/2.11.0.4/pandoc-2.11.0.4-1-amd64.deb)

### Mac OS

使用Homebrew：

    brew install pandoc

或下载[pandoc-2.11.0.4-macOS.pkg](https://github.com/jgm/pandoc/releases/download/2.11.0.4/pandoc-2.11.0.4-macOS.pkg)

### Windows x86_64

[pandoc-2.11.0.4-windows-x86_64.msi](https://github.com/jgm/pandoc/releases/download/2.11.0.4/pandoc-2.11.0.4-windows-x86_64.msi)

## 2. 创建书籍

1. 切换到此目录。
2. 用你自己的内容替换`title.md`和封面图像`images/cover.png`。
3. 在`contents`目录中写markdown（文件名不能带空格），或者按你的喜好创建目录和子目录。
4. 将其他图像放入“images”目录。
5. 运行`export-epub`或者其他脚本。

输出为`book.epub`。

注意: 如果给定了多个输入文件，在解析之前pandoc将按照 **文件列表的顺序** 将它们全部连接起来（之间有空行）。
