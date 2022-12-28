# 贡献指南

:sparkles: 首先，感谢您的贡献！

可以通过Issue或PR提交钩子，但前提要求是：

- 开源且README包含使用说明或有文档

- 基本稳定，无明显Bug，且积极开发维护

- 支持Python3.8+

## 通过Issue提交

请 [新建Issue](https://github.com/sapicd/awesome/issues/new?assignees=&labels=enhancement&template=newhook.md&title=%5BPR%5D)，按照模板提供信息，由作者添加。

## 通过PR提交

请 Fork 本项目（如已fork也请[同步下源仓库](https://docs.github.com/cn/github/collaborating-with-issues-and-pull-requests/syncing-a-fork)），修改如下文件：

1、【必填】list.json

这是标准的JSON格式文件，所以你填写的内容要符合标准，否则会导致异常。

其内容是一个列表，在列表末追加以下内容（在末尾 **]** 括号前面，如多个则追加多个）：

```
    ,{
        "name": "[必填]<Name>",
        "module": "[必填]<Module_Name>",
        "desc": "[必填]一句话描述",
        "github": "[必填]<User>/<Repo>",
        "pypi": "$name",
        "status": "<beta rc stable/production/ga archive>"
    }
```

注意前有逗号，后无逗号，且内部最后一个字段无逗号，多一个少一个都是非法的。

按照 **<>** 内提示填写，注意必填项，特别说明以下字段：

- module: 程序可在Python中直接导入的模块名称

- pypi: 可移除、留空字段，特殊值 `$name` 表示同name

- status: 程序状态，至少beta公测版本，rc是预发布，后三者是稳定版，archive是封存

- author: 作者，没有在上述内容中限定，因为其默认是github的 `<User>` 部分

- home: 作者网站，同author，默认是 ``https://github.com/<User>``

- catalog: 分类，即为模块文件内 ``__catalog__ `` ，比如upload（暂未用到）

填写完成，最好是格式化一下。

2、【建议】README.md

在 **列表** 的表格下添加：

`| [<Name>](<GitHub>) | <描述> |`

--------

发起Pull Request
