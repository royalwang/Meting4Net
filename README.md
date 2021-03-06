<p align="center">
<img src="docs/_images/Meting4Net.png" alt="Meting4Net">
</p>
<h1 align="center">Meting4Net</h1>

> :cake: 一个强大的音乐API框架

[![repo size](https://img.shields.io/github/repo-size/yiyungent/Meting4Net.svg?style=flat)]()
[![LICENSE](https://img.shields.io/github/license/yiyungent/Meting4Net.svg?style=flat)](https://mit-license.org/)
[![nuget](https://img.shields.io/nuget/v/Meting4Net.svg?style=flat)](https://www.nuget.org/packages/Meting4Net/)
[![downloads](https://img.shields.io/nuget/dt/Meting4Net.svg?style=flat)](https://www.nuget.org/packages/Meting4Net/)


[English](README_en.md)

## 介绍

Meting4Net: <a href="https://github.com/metowolf/Meting" target="_blank">Meting</a> for .Net, thanks to <a href="https://github.com/metowolf/Meting" target="_blank">Meting</a>.   

一个强大的音乐API框架促进你的开发
 + **优雅** - 简单易用, 对于所有平台均可一个标准格式.
 + **丰富** - 支持多个音乐平台, 包括 腾讯QQ音乐, 网易云音乐, 虾米音乐, 酷狗, 百度等.
 + **免费** - MIT协议 发布
 
## 进度

- [x] 网易云音乐 Meting Open API 移植完成 v0.1.0
- [x] 腾讯QQ音乐 Meting Open API 移植完成 v0.2.0
- [x] 酷狗音乐 Meting Open API 移植完成 v1.0.0

## 需要

只需要满足下方其中一条.

- .NET Framework (>= 4.5) 且 Newtonsoft.Json (>= 12.0.1) 被安装.
- .NET Standard (>= 2.0) 且 Microsoft.CSharp (>= 4.5.0), Newtonsoft.Json (>= 12.0.1) 被安装.

## 安装

推荐使用 [NuGet](https://www.nuget.org/packages/Meting4Net), 在你项目的根目录 执行下方的命令, 如果你使用 Visual Studio, 这时依次点击 **Tools** -> **NuGet Package Manager** -> **Package Manager Console** , 确保 "Default project" 是你想要安装的项目, 输入下方的命令进行安装.

```bash
PM> Install-Package Meting4Net
```

## 快速开始

```csharp
using Meting4Net.Core;
   ...
// 初始化 网易云音乐API
Meting api = new Meting("netease");
// 获得 json 数据
string jsonStr = api.FormatMethod(true).Search("Soldier", new Meting4Net.Core.Models.Standard.Options
{
    page = 1,
    limit = 50
});

return Content(jsonStr, "application/json");
//[{"id":35847388,"name":"Hello","artist":["Adele"],"album":"Hello","pic_id":"1407374890649284","url_id":35847388,"lyric_id":35847388,"source":"netease"},{"id":33211676,"name":"Hello","artist":["OMFG"],"album":"Hello",...
```

## 环境

- 运行环境: .NET Framework (>= 4.5) or .NET Standard (>= 2.0)    
- 开发环境: Visual Studio Community 2017

## 相关项目

 - [Meting](https://github.com/metowolf/Meting)
 
 