# 贡献指南

所有的面试题都存放在 [`data/questions`](https://github.com/f2eso/interview/tree/master/data/questions) 目录下。此目录下的文件夹为面试题所归属的「[主题](https://fes.ourai.ws/interview/subjects/)」，它们分别为：

| 文件夹 | 主题 | 描述 |
| --- | --- | --- |
| `web-design` | [网页设计](https://fes.ourai.ws/interview/subjects/web-design/) | - |
| `programming` | [程序设计](https://fes.ourai.ws/interview/subjects/programming/) | - |
| `browser` | [浏览器](https://fes.ourai.ws/interview/subjects/browser/) | - |
| `security` | [网络安全](https://fes.ourai.ws/interview/subjects/security/) | - |
| `engineering` | [前端工程](https://fes.ourai.ws/interview/subjects/engineering/) | - |
| `framework` | [库与框架](https://fes.ourai.ws/interview/subjects/framework/) | - |
| `communication` | [网络通信](https://fes.ourai.ws/interview/subjects/communication/) | - |
| `language` | [编程语言](https://fes.ourai.ws/interview/subjects/language/) | - |
| `tool` | [工具](https://fes.ourai.ws/interview/subjects/tool/) | - |

每个主题目录下的文件夹是面试题，再往下则是某个面试题相关的数据文件。因此，一个面试题的数据文件路径是 `data/questions/{主题}/{面试题}/{数据文件}`。

主题和面试题的文件夹名字要尽可能简短，且尽量不是句子，更不能是问句；面试题相关数据文件的命名方式与作用如下：

| 文件 | 作用 | 必需 |
| --- | --- | --- |
| `metadata.yml` | 问题标题等元数据 | 是 |
| `readme.md` | 问题描述 | 是 |
| `answer.md` | 问题回答 | 否 |
| `explain.md` | 问题讲解 | 否 |

在严格遵守上述内容的前提下，可以通过提 [PR](https://github.com/f2eso/interview/pulls) 新建或修改一个主题、面试题及其相关的数据文件。
