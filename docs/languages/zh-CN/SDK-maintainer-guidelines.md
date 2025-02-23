# SDK 维护者指南

语言: [English](../../docs/SDK-maintainer-guidelines.md) | [简体中文](SDK-maintainer-guidelines.md)

<!-- no verify-specs -->

本指南旨在为 SDK 维护人员提供一些常见的推荐方法
实践。鼓励新的和现有的 SDK 维护人员复制此文件
到他们的存储库，并采用这些指导方针，以便贡献者可以
希望每个 SDK 都有共同的体验。

## 技巧

这些提示旨在帮助防止问题和拉请求
陈旧和过时的。

- 掌握你自己的拉请求。pr 如果停滞太久，就很难合并。
- 从你自己的叉子。当你为项目做出贡献时，你应该像外部贡献者一样从自己的分支工作。这使得 github 中的分支最小化，并减少了不必要的 CI 运行。
- 主动标注问题，用相关和描述性的标签拉出请求。
- 积极审查提交的拉请求。一个拉请求不应该在没有评论或审查的情况下持续超过几天。
- 经常出现分诊问题。
- 如果一些问题因为不再有效/相关或讨论没有达成重要的行动项目而过时太久，关闭该问题，并邀请用户在需要时重新打开它。
- 如果一些 PR 由于冲突而不再有效，但 PR 仍然需要，要求贡献者从主分支重新建立他们的 PR。
- 如果你发现一个问题，你想创建一个拉请求，一定要分配给你自己的问题，以便其他维护者不开始在同一时间工作。
- 考虑使用 GitHub 动作主动标记并最终关闭旧的问题，并在它们变得过时时拉出请求。

## 提交的信息

使用[常规提交规范](https://www.conventionalcommits.org/en/v1.0.0/)
当写入提交消息时。这个约定与[SemVer](http://semver.org/)一起工作得很好。
通过描述提交消息中的特性、修复和破坏更改。通过构建
您的提交消息以这种方式，它们有效地传达了意图和效果
存储库提交给库的消费者。

简单地说，提交消息的结构应该是:

```
<type>[optional scope]: <description>

[optional body]

[optional footer]
```

当在你的提交中使用'——signff '时，页脚将是你的 signff。例如:

```
    Signed-off-by: Joe Smith <joe.smith@email.com>
```

的其他详细信息，请参阅常规提交规范
提交消息中的结构细节，如“类型”和“范围”。

## 着陆拉请求

当降落拉请求时，一定要检查提交的第一行
使用适当的提交消息前缀。例如，如果它是一个文档
更改，使用"docs:"作为提交消息的前缀。

如果有超过一次提交，试着压缩成一次提交。通常这是可以做到的当合并 PR 时使用 GitHub UI。使用“挤压和合并”。以确保社区中的每个人都有机会回顾和评论拉请求，通常在拉请求之后有一些时间是很好的提交，在它落地之前。

以下是关于 pull 请求批准和时间安排的一些指导方针。

- 没有通过所有自动检查的拉请求不能降落

- 所有的拉起请求在着陆前至少需要一个维护人员的批准

- pull request 的作者可以批准他们自己的 PR，但需要额外的批准才能着陆

- 如果一个维护者提交了一个拉请求，并且它没有得到至少一个其他维护者的批准，它可以在 72 小时后降落

- 如果一个拉请求同时获得批准和请求更改，在请求更改解决之前它不能被降落

## 部门管理

“主要”分支是最前沿的。库的新主版本

都是从这支树枝上剪下来的。如果你打算提交撤销请求

你应该用“main HEAD”作为你的起点。

每个主要版本都应该产生一个新的分支和标记。例如,

库的版本 1.0.0 的发布将导致在

释放提交，和一个新的分支' v1.x。Y '表示后续小调和补丁

主要版本的级别发行版。然而，发展仍将继续

快速使用' main '来开发下一个主要版本——例如 2.0.0。版本分支

仅为每个主要版本创建。次要版本和补丁级别版本

只是标记。
