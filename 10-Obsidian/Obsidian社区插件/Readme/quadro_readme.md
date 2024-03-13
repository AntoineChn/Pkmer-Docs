---
uid: 2024031219330710
title: Obsidian 插件：【Readme】Quadro
tags: ['obsidian插件', 'readme']
description: 定性数据分析（QDA）适用于社会科学家。这是MAXQDA和atlas.ti的开放替代方案，使用Markdown来存储数据和研究代码。
author: AI
type: readme
draft: false
editable: false
modified: 20230101000000
---

# Obsidian 插件：【Readme】Quadro

> [!Note] 插件名片
> - 插件名称：Quadro
> - 插件作者：Chris Grieser (aka pseudometa)
> - 插件说明：定性数据分析（QDA）适用于社会科学家。这是 MAXQDA 和 atlas.ti 的开放替代方案，使用 Markdown 来存储数据和研究代码。
> - 插件分类：['obsidian 插件 ', 'readme']
> - 项目地址：[点我访问](https://github.com/chrisgrieser/obsidian-quadro)
> - 国内下载地址：[下载安装](https://pkmer.cn/products/plugin/pluginMarket/?quadro)

## 概述

定性数据分析（QDA）适用于社会科学家。这是 MAXQDA 和 atlas.ti 的开放替代方案，使用 Markdown 来存储数据和研究代码。

> [!tip] 原文出处
>
>下面自述文件的来源于 [Readme](https://ghproxy.net/https://raw.githubusercontent.com/chrisgrieser/obsidian-quadro/main/README.md)

---

## Readme(翻译）

下面是 [[quadro]] 插件的自述翻译

【机翻】

# Quadro- 在 Obsidian 中实现的定性数据分析

![GitHub下载次数](https://img.shields.io/github/downloads/chrisgrieser/obsidian-quadro/total?label=GitHub下载次数&style=plastic)

![Obsidian商店下载次数](https://img.shields.io/badge/dynamic/json?logo=obsidian&color=%23483699&label=Obsidian下载次数&query=%24%5B%22quadro%22%5D.downloads&url=https%3A%2F%2Fraw.githubusercontent.com%2Fobsidianmd%2Fobsidian-releases%2Fmaster%2Fcommunity-plugin-stats.json&style=plastic)

![最新版本](https://img.shields.io/github/v/release/chrisgrieser/obsidian-quadro?label=最新版本&style=plastic)

Obsidian 插件，用于社会科学定性数据分析（QDA）。是 [ MAXQDA ](https://www.maxqda.com/) 和 [atlas.ti](https://atlasti.com/) 的开放替代方案，使用 Markdown 来存储数据和研究代码。

*Quadro*支持*Grounded Theory*风格的编码和*Qualitative Content Analysis*风格的提取。

## 目录

<!-- toc -->

- [介绍](#introduction)

	* [对于不熟悉Obsidian的学者](#for-academics-not-familiar-with-obsidian)
	* [对于不熟悉QDA的Obsidian用户](#for-obsidian-users-not-familiar-with-qda)
	* [与其他QDA软件的简要方法比较](#brief-methodological-comparison-with-other-qda-software)

- [用法](#usage)

	* [入门](#getting-started)

		+ [示例Vault](#example-vault)
		+ [经验丰富的Obsidian用户](#experienced-obsidian-users)
		+ [使用单独的Vault](#using-a-separate-vault)
		+ [从其他QDA软件的现有研究项目迁移](#migrating-from-an-existing-research-project-with-other-qda-software)

	* [编码](#coding)

		+ [Quadro中编码的工作原理](#how-coding-works-in-quadro)
		+ [编码功能](#coding-capabilities)

	* [提取](#extraction)

		+ [Quadro中提取的工作原理](#how-extraction-works-in-quadro)
		+ [聚合提取](#aggregate-extractions)
		+ [提取功能](#extraction-capabilities)

- [技术](#technical)

	* [要求](#requirements)
	* [安装](#installation)
	* [更新](#update)
	* [错误报告和功能请求](#bug-reports--feature-requests)
	* [开发](#development)

- [鸣谢](#credits)

	* [致谢](#acknowledgments)
	* [推荐引用此项目](#recommended-citation-of-this-project)
	* [关于开发者](#about-the-developer)

<!-- tocstop -->

## 介绍

### 对于不熟悉 Obsidian 的学者

这个插件利用了 [Obsidian](https://obsidian.md/) 的丰富文本处理功能，为定性数据分析提供了一个轻量级的应用程序。

所有数据都存储为 [Markdown](https://www.markdownguide.org/) 文件。

**Markdown** 是一种人类可读、非专有且常用的开放标准，用于纯文本文件。这意味着：

- 没有锁定/依赖于特定软件，数据可以在支持 Markdown 的任何应用程序中进行分析。（实际上，数据存储在纯文本中，因此甚至可以使用 `Notepad.exe` 或 `TextEdit.app` 打开和阅读）
- 研究数据因此具有未来性，满足了定性数据的长期存档要求。可以保证数据即使在 50 年后仍然可以阅读，这是专有研究软件（如 `MAXQDA` 或 `atlas.ti`）所不具备的保证。
- 数据与其他应用程序具有互操作性，这意味着它可以轻松地与其他文本分析工具（如 [AntConc](https://www.laurenceanthony.net/software/antconc/)）或浏览器扩展（如 [MarkDownload](https://chromewebstore.google.com/detail/markdownload-markdown-web/pcmpcfapbekmbjjkdalcgopdkipoggdi)）结合使用，以获取网站内容。
- Markdown 文件默认存储在离线状态，满足了研究伦理和研究数据保护的关键要求。

作为 Obsidian 插件，定性数据分析嵌入在 Obsidian 的广泛功能和插件生态系统中：

- 数据分析可以利用 Obsidian 的功能集，该功能集已经专注于链接文件。例如，[图形视图](https://help.obsidian.md/Plugins/Graph+view) 可用于创建代码的可视化网络，而 [Outgoing Links](https://help.obsidian.md/Plugins/Outgoing+links) 提供了代码分配给的所有数据文件的概述。
- 定性分析可以轻松扩展到一个 [超过1000个插件的全面生态系统](https://obsidian.md/plugins)，例如用于高级数据聚合的 [DataLoom](https://obsidian.md/plugins?id=notion-like-tables) 或用于自动获取 YouTube 视频转录的 [YTranscript](https://obsidian.md/plugins?id=ytranscript)。
- 所有这些都允许研究人员根据其研究的特定需求定制分析。研究方法的案例特定调整是定性研究的一个关键需求（在使用标准化的专有研究软件时，这个需求严格来说并没有真正得到满足）。
- Obsidian 和 *Quadro* 都 [支持移动设备（Android 和 iOS）](https://obsidian.md/mobile)。
- 使用 Obsidian 可以采用以键盘为驱动的工作流程，最小化鼠标的使用。

如果研究团队中有更懂技术的研究人员，*Quadro* 的优势甚至更大：

- 作为开源软件，这个插件可以被修改和定制以满足他们的需求。（它是用 TypeScript / JavaScript 编写的，这是一种特别易于访问和常用的编程语言。）
- 通过将数据存储在 markdown 文件中，所有研究数据都可以通过 `git` 进行完全版本控制。

Obsidian 是 [免费供学术用途使用的](https://obsidian.md/license)，*Quadro* 也是免费使用的。特别是对于撰写论文的学生，这可以节省许多不必要的许可证麻烦。

### 对于不熟悉 QDA 的 Obsidian 用户

在定性数据分析中，“编码”是对文本段进行细粒度标记的一种形式，“提取”是将散文文本转化为结构化数据。

*编码*是通过在数据文件和代码文件之间插入 wikilinks 来实现的，这种“双向”链接。 （Obsidian 本身确实有反向链接，但这些是单向链接，因为隐式的反向链接仅被推断而不存储在任何地方的 markdown 文件中。）。

它利用 Obsidian 的 [note-embedding](https://help.obsidian.md/Linking+notes+and+files/Embed+files#Embed+a+note+in+another+note) 功能来跟踪编码的文本段。

- 代码是以 `[[wikilinks]]` 的形式实现的，而不是 `#tags`，因为前者允许更灵活，比如每个代码一个单独的文件。
- 这个插件的独特特点是，它的命令*总是*同时编辑两个文件（数据文件和代码文件），这对于充分处理 QDA 中常见的编码工作流程是必要的。

*提取*是通过为每个提取创建单独的提取文件来实现的，使用 [YAML frontmatter](https://docs.zettlr.com/en/core/yaml-frontmatter/) 来以结构化形式存储数据。 Quadro 使用简单的模板机制来支持这些提取文件的创建。

### 与其他 QDA 软件的简要方法论比较

**优势**

- **互操作性**：可以自由与其他 QDA 软件结合使用。
- **灵活性**：您可以使用代码、提取或自由组合两者。
- **可定制性**：QDA 软件的隐含假设，比如代码选择模态中代码呈现的初始顺序，可以定制以处理不同类型的编码者偏见。
- **可扩展性**：*Quadro*可以通过 Obsidian 插件生态系统轻松扩展。与其他研究软件不同，在大多数情况下扩展功能不需要技术专业知识编码经验。

**劣势**

- **编码单位**仅限于段落，到一定程度上也包括段落的片段。不支持对单个单词进行编码。
- 由于 Markdown 标记的特性，无法将多个代码分配给**部分重叠的段落片段**。这个限制仅适用于部分重叠，当然可以将多个代码分配给同一段落或段落片段。

## 用法

### 开始使用

#### 示例保险库

有一个 [预先配置的示例保险库](https://github.com/chrisgrieser/obsidian-quadro) 可用于*Quadro*。除了一些预安装的 QDA 插件外，它还包括一些带有示例代码和提取的模拟数据，并展示了提取功能，以展示*Quadro*的功能。

1. [下载保险库](https://github.com/chrisgrieser/quadro-example-vault/releases/latest/download/quadro-example-vault.zip)。
2. 将目录 `quadro-example-vault` 作为 Obsidian 保险库打开。([如果您是Obsidian的新手，请参阅Obsidian文档以了解如何进行操作。](https://help.obsidian.md/Getting+started/Create+a+vault#Open+existing+folder))

#### 有经验的黑曜石用户

如果您对黑曜石很有经验，您也可以 [直接安装插件](#installation)，不过查看示例保险库仍然是有帮助的，以便更好地了解*Quadro*的功能。

#### 使用单独的保险库

建议为数据分析创建一个单独的保险库，并在那里安装插件，原因如下：

- QDA 不遵循“笔记常规逻辑”，因此通常需要与常规保险库不同的插件和设置。
- 单独的保险库意味着建议（例如属性）也是分开的。
- 为了使 Obsidian 更易于用于定性研究，*Quadro*还对 Obsidian 的核心布局进行了一些（轻微的）修改，例如更宽的属性键。
- 出于档案目的，研究数据已经分开。
- 对于研究团队中的协作工作，数据与个人笔记分开存储。
很遗憾，这是不支持的。主要原因是商业 QDA 软件使用专有格式，这也是研究人员应该一开始就使用开放格式的研究软件的确切原因。

如果您的研究数据保存在 [Markdown中，Obsidian可以导入它们](https://help.obsidian.md/import/markdown)。同时，也支持从 [各种其他笔记应用程序，如Notion、Evernote、OneNote、Google Keep、Apple Notes、Bear或Roam](https://help.obsidian.md/import) 导入。

然而，可以将使用*Quadro*完成的结果导出，以便与其他研究人员合作。您可以将单个文件导出为 PDF，或者 [将聚合结果导出为CSV](#extraction-capabilities)。

### 编码

#### 在 Quadro 中编码的工作原理

分析中有两种基本类型的文件，数据文件和代码文件，它们都以 [Markdown文件](https://www.markdownguide.org/) 的形式存储。

**数据文件**

作为文本文件的经验材料。它们可以存储在保险库中的任何位置，以 `.md` 文件的形式存储。（建议单独创建一个名为 `Data` 的子文件夹。）由于*Quadro*将代码分配给整个段落，因此这些数据文件应该被分割成更小的段落。

当分配代码时，会在段落末尾附加指向相应代码文件和唯一 ID 的链接：

```md
文件名: ./Data/Interview 1.md

Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint
consectetur cupidatat. [[MyCode]] ^id42
```

**代码文件**

文件夹 `{vault-root}/Codes` 中的所有 Markdown 文件都被视为代码文件。

当分配代码时，会在代码文件中附加指向数据文件中原始位置的链接。

```md
文件路径: ./Codes/MyCode.md

![[Interview 1#^id42]]
```

由于该链接是所谓的 [嵌入链接](https://help.obsidian.md/Linking+notes+and+files/Embed+files#Embed+a+note+in+another+note)，Obsidian 会在代码文件中呈现数据文件的相应段落：

![在阅读和源模式下的嵌入块链接](https://cdn.pkmer.cn/covers/quadro_2_0.png!pkmer)

用于编码的基础文件夹结构如下（颜色代表代码）：

```txt
.
├── 📂 Data
│   ├── 📄 Interview 1.md
│   ├── 📄 Field Notes 1.md
│   └── …
└── 📂 Coding
    ├── 📄 blue.md
    ├── 📄 red.md
    └── 📂 Group 1
         ├── 📄 white.md
         ├── 📄 black.md
         └── …
```

> [!NOTE]
> 这种方法的主要缺点是代码的分配主要限制在段落级别。仅将代码分配给段落的部分限于向相应部分添加高亮显示。不支持将代码分配给单个单词和具有重叠的编码段。

#### 编码能力

| 操作                                    | 描述                                                                                                                                                                                                                            |             侧边栏按钮             | 默认快捷键 | 能力提供者                       |
| ----------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------: | :------------: | ----------------------------------------- |
| 分配代码                               | 为当前段落分配一个代码，任何选定的文本都会被突出显示。（不支持重叠的突出显示）。<br><br>选择 `创建新代码` 或按 `shift ⏎` 创建一个新的代码文件并将其分配给段落。 |   ![Icon](./assets/plus-circle.svg)    | `mod+shift+a`  | Quadro                                    |
| 重命名代码                               | 所有对代码文件的引用都会自动更新。（您也可以右键单击文件或链接并选择“重命名”来重命名。）                                                                                              |   ![Icon](./assets/circle-slash.svg)   | `mod+shift+r`  | [Obsidian 内置][rename]               |
| 从段落中删除代码                | 从数据文件或代码文件的当前段落中删除代码。相应的其他文件中的引用也会被删除。                                                                                                |   ![Icon](./assets/minus-circle.svg)   | `mod+shift+d`  | Quadro                                    |
| 删除代码文件及其所有引用 | 将代码文件移动到垃圾箱，并删除所有对它的引用。                                                                                                                                                                  |     ![Icon](./assets/x-circle.svg)     |       —        | Quadro                                    |
| 批量创建新代码                     | 一次创建多个新代码（而不将它们分配给段落）。                                                                                                                                                             |  ![Icon](./assets/circle-dashed.svg)   |       —        | Quadro                                    |
| 代码分组                             | 可以通过文件资源管理器中的拖放来将代码排列在子文件夹中。                                                                                                                                                            |                   —                    |       —        | [Obsidian 内置][move file]            |
| 代码关系可视化       | 在图形视图中，使用类似 `path:Codes OR path:Data` 的查询，并将数据和代码分配给不同的组。<br><br>[更多文档][graph]                                                                                   |     ![Icon](./assets/git-fork.svg)     |    `mod+g`     | [Obsidian 核心插件: 图形视图][graph] |
| 轴向编码                              | 使用 Canvas 插件，您可以在面板上自由排列实体，并通过线条和箭头连接它们，适用于轴向编码。<br><br>[更多文档][canvas]                                                         | ![Icon](./assets/layout-dashboard.svg) |       —        | [Obsidian 核心插件: Canvas][canvas]    |
| 代码共现的调查      | 在 Obsidian 搜索中，使用查询如 `line:([[MyCodeOne]] [[MyCodeTwo]])`。<br><br>[更多文档][search]                                                                                                              |                   —                    | `mod+shift+f`  | [Obsidian 核心插件: 搜索][search]    |

[rename]: <https://help.obsidian.md/Files+and+folders/Manage+notes#Rename+a+note>
[graph]: <https://help.obsidian.md/Plugins/Graph+view>
[search]: <https://help.obsidian.md/Plugins/Search#Search+operators>
[move file]: <https://help.obsidian.md/Plugins/File+explorer#Move+a+file+or+folder>
[canvas]: <https://help.obsidian.md/Plugins/Canvas>

- `mod` 在 Windows 上指 `ctrl`，在 macOS 上指 `cmd`。每个快捷键都可以通过在 Obsidian 快捷键设置中搜索相应操作的名称来自定义。
- 尚不支持拆分和合并代码文件。使用任何其他方法（如插件）进行此操作可能会导致引用损坏。
- ⚠️ 重命名或移动代码/数据文件应该在 Obsidian 内部完成。使用 Windows 资源管理器或 macOS 的 Finder 不会触发引用的自动更新，意味着信息丢失。

### 提取

#### Quadro 中的提取工作原理

提取的实现方式与编码类似，使用两种基本文件类型，数据文件和提取文件。

**数据文件**

实证材料以文本文件形式存在。它们可以存储在保险库中的任何位置，以 `.md` 文件的形式。

在进行提取时，会像编码一样，在段落末尾附加指向相应提取文件和唯一 ID 的链接：

```md
文件名: ./Data/Interview 2.md

Lorem ipsum dolor sit amet, qui minim labore adipisicing minim sint cillum sint
consectetur cupidatat. [[Career Visions/1]] ^id-481516
```

**提取文件**

提取是通过 Markdown 元数据（[YAML frontmatter](https://docs.zettlr.com/en/core/yaml-frontmatter/)）实现的，

通过 [Obsidian Properties](https://help.obsidian.md/Editing+and+formatting/Properties) 支持。

在进行提取时，您可以选择提取类型。选择后，将在分组提取的文件夹中创建一个新文件，即 `{vault-root}/Extractions/{Extraction Group}/`。

因此，每个文件对应一个单独的提取，其父文件夹指示其是何种类型的提取。

然后，您可以填写新创建文件的字段。

`extraction source` 键包含一个链接，返回到您发起提取的数据文件中的位置。

在渲染视图中，文件包含一个方便填写的 `Properties` 头部：

![展示提取](https://cdn.pkmer.cn/covers/quadro_2_8.png!pkmer)

文件的底层纯文本视图如下所示：

```md
文件路径: ./Extractions/Career Visions/Career Visions 1.md

---
occupation: "painter"
career stage: "novice"
year of experience: 4
extraction date: 2024-02-12
extraction source: "[[Field Notes 3]]"
---

**提取自段落：** ![[Field Notes 3#^id-42]]
```

**提取模板（提取类型）**

可用的提取类型由 `{vault-root}/Extractions/` 的子文件夹确定。

用于填写信息的字段由该子文件夹中的 `Template.md` 文件确定。

对于上述示例，提取模板如下所示：

相应提取类型的模板位于同一文件夹中，但文件名为 `Template.md`。

```md
文件路径: ./Extractions/Career Visions/Template.md

---
occupation: 
career stage: 
year of experience: 
---
```

总的来说，提取的底层文件夹结构如下所示：

```txt
.
├── 📂 Data
│   ├── 📄 Interview 1.md
│   ├── 📄 Field Notes 1.md
│   └── …
└── 📂 Extractions
    ├── 📂 Career Obstacles
    │    ├── 📄 Template.md
    │    ├── 📄 Career Obstacles 1.md
    │    ├── 📄 Career Obstacles 2.md
    │    └── …
    └── 📂 Career Visions
         ├── 📄 Template.md
         ├── 📄 Career Visions 1.md
         └── …
```

#### 聚合提取

使用 `Aggregate extractions` 命令创建一个可以排序、过滤、搜索和修改的表格：

<https://github.com/chrisgrieser/obsidian-quadro/assets/73286100/6242a113-b17e-42e3-9398-806cdbec3b2d>

#### 提取功能

| 操作                               | 描述                                                                                                                                                                                                                                                                                                          |            侧边栏按钮             | 默认快捷键 | 提供功能的插件                                      |
| ---------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-----------------------------------: | :------------: | -------------------------------------------------------- |
| 从段落中提取                      | 从提取模板创建一个提取文件。                                                                                                                                                                                                                                                            |   ![Icon](./assets/plus-square.svg)   | `mod+shift+e`  | Quadro                                                   |
| 创建新的提取类型                  | 创建一个新的提取类型（在“提取”中创建一个新的子文件夹，以及一个新的提取模板）。                                                                                                                                                                                                        |   ![Icon](./assets/box-select.svg)    |       —        | Quadro                                                   |
| 聚合提取                          | 创建一个汇总提取文件的表格。该表格可以进行排序、筛选、搜索和修改。<br><br>[更多文档][data loom]                                                                                                                                                         |  ![Icon](./assets/sigma-square.svg)   |       —        | [社区插件: Data Loom][data loom]                 |
| 共同提取维度                     | 通过在 Obsidian 搜索中使用类似 `["问题原因": 碎片化] ["兼容性类型": 向后]` 的查询，找到两个维度具有特定值的提取。<br><br>[更多文档][search]                                                                                |                   —                   | `mod+shift+f`  | [Obsidian 核心插件: 搜索][search]                   |
| 全局重命名维度                   | 在文件中重命名属性字段仅影响该文件的属性。要全局重命名属性，请使用命令面板（`mod+p`），并搜索 `Properties View: Show all Properties`。侧边栏中会弹出一个属性列表，您可以通过右键单击重命名属性。         |                   —                   |       —        | [Obsidian 核心插件: 属性视图][properties view] |
| 将所有提取导出为 `.csv`            | 将所有提取类型的所有提取导出为以 `,` 分隔的 `.csv` 文件。                                                                                                                                                                                                                                  | ![Icon](./assets/arrow-up-square.svg) |       —        | Quadro                                                   |

[data loom]: <https://dataloom.xyz/>
[properties view]: <https://help.obsidian.md/Plugins/Properties+view>

- `mod` 在 Windows 上指 `ctrl`，在 macOS 上指 `cmd`。每个快捷键都可以通过在 Obsidian 快捷键设置中搜索相应操作的名称来自定义。
- 对于聚合和 `.csv` 导出，包含的属性由模板文件（`Template.md`）的属性决定。
- ⚠️ 重命名或移动提取/数据文件应该在 Obsidian 内部完成。使用 Windows 资源管理器或 macOS 的 Finder 不会触发自动更新引用，意味着信息丢失。

## 技术

### 要求

*Quadro* 需要至少 **Obsidian 版本 1.5.8**。

*Aggregate Extractions* 命令需要 [DataLoom 插件](https://obsidian.md/plugins?id=notion-like-tables)。

### 安装

**手动安装**

1. [下载最新版本](https://github.com/chrisgrieser/obsidian-quadro/releases/latest/download/obsidian-quadro.zip)。
2. 将 `.zip` 文件解压到文件夹 `{your-vault-path}/.obsidian/plugins/quadro` 中。（请注意，在 macOS 上，`.obsidian` 是一个隐藏文件夹。您可以通过在 Finder 中按下 `cmd+shift+.` 来使隐藏文件夹可见。）
3. 在 Obsidian 中，转到 `设置`→`社区插件`。点击刷新按钮。
4. 在插件列表中查找新条目 `Quadro`。通过勾选框启用插件。

**BRAT（Beta Reviewers Auto-update Tester）**
或者，如果您已经熟悉 Obsidian 生态系统，您也可以通过 [BRAT](https://github.com/TfTHacker/obsidian42-brat) 安装插件。

**Obsidian 社区插件商店**
一旦在 Obsidian 社区插件商店中发布，*Quadro* 将可以通过 Obsidian 的插件浏览器访问：`设置`→`社区插件`→`浏览`→搜索 *"Quadro"*

### 更新

**手动**

1. 关闭 Obsidian。
2. 从 [最新版本](https://github.com/chrisgrieser/obsidian-quadro/releases/latest) 下载 `.zip` 文件。
3. 将 `.zip` 文件解压到 `{your-vault-path}/.obsidian/plugins/quadro`，替换该文件夹中的现有文件。
4. 再次启动 Obsidian。

**BRAT**
如果您通过*BRAT*添加了插件，它会在每次启动 Obsidian 时自动检查新的更新，并在有新版本可用时自动更新*Quadro*。

**Obsidian 社区插件商店**
一旦在 Obsidian 社区插件商店中发布，您可以通过以下方式更新*Quadro*（以及您安装的所有其他插件）：`设置` → `社区插件` → `检查更新` → `全部更新`。

### Bug Reports & Feature Requests

- 对于 bug 报告或功能请求，请使用 [GitHub问题跟踪器](https://github.com/chrisgrieser/obsidian-quadro/issues)。
- 对于关于*Quadro*的问题和一般讨论，请使用 [GitHub讨论论坛](https://github.com/chrisgrieser/obsidian-quadro/discussions)。

### 开发

```bash
git clone "git@github.com:chrisgrieser/obsidian-quadro.git"
make init
```

```bash
make format    # 运行所有格式化程序
make build     # 构建插件
make check-all # 运行预提交钩子（不提交）
```

> [!NOTE]
> 该存储库使用预提交钩子，防止未通过所有检查的提交。

## 鸣谢

### 致谢

- [Ryan Murphy](https://fulcra.design/About/) 给了我这个项目的创意，他在他的 [博客文章](https://fulcra.design/Posts/An-Integrated-Qualitative-Analysis-Environment-with-Obsidian/) 中提到了这个想法。
- [Grit Laudel](http://www.laudel.info/) 提供了样本访谈数据。

### 该项目的推荐引用

请按照以下 APA 格式引用此软件项目：

```txt
Grieser, C. (2024). Quadro – Qualitative Data Analysis Realized in Obsidian [Computer software]. 
https://github.com/chrisgrieser/obsidian-qualitative-data-analysis
```

对于其他引用样式，请使用以下元数据：

- [引用文件格式（.cff）](./recommended-citation/CITATION.cff)
- [BibTeX（.bib）](./recommended-citation/CITATION.bib)

### 关于开发者

我是一名社会学家，研究数字经济背后的社会机制。在我的博士项目中，我调查了应用经济的治理以及软件生态系统如何管理创新和兼容性之间的紧张关系。如果您对这个主题感兴趣，请随时与我联系。

- [学术网站](https://chris-grieser.de/)
- [ResearchGate](https://www.researchgate.net/profile/Christopher-Grieser)
- [Discord](https://discordapp.com/users/462774483044794368/)
- [GitHub](https://github.com/chrisgrieser/)
- [Twitter](https://twitter.com/pseudo_meta)
- [Mastodon](https://pkm.social/@pseudometa)
- [LinkedIn](https://www.linkedin.com/in/christopher-grieser-ba693b17a/)

*如有错误报告和功能请求，请使用 [GitHub问题跟踪器](https://github.com/chrisgrieser/obsidian-quadro/issues)。*

<a href='https://ko-fi.com/Y8Y86SQ91' target='_blank'>
<img height='36' style='border:0px;height:36px;'
src='https://cdn.ko-fi.com/cdn/kofi1.png?v=3' border='0' alt='在ko-fi.com给我买杯咖啡'/></a>



