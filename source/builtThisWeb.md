# Refence
## Git

1. [Git使用总结(包含Git Bash和Git GUI的使用)](https://blog.csdn.net/KevinDGK/article/details/51606925?spm=1001.2014.3001.5502)
2. [Git error: failed to push some refs to](https://www.jianshu.com/p/c6f2e1ca2999)
本地与远程产生冲突:
- 强覆盖  `git push -f origin master`
- 拉取再提交; `--rebase` 到底是干嘛用的
'''
  git pull –-rebase origin maste
  git push origin master
'''

## mkdocs

### Tutrial
1. [Blog_Mkdocs 配置和使用](https://www.xncoding.com/2020/03/01/tool/mkdocs.html)
2. [少数派_MkDocs 快速上手指南](https://sspai.com/prime/story/mkdocs-primer)
### other might help
1. [搭建个人博客，你需要知道这些](https://zhuanlan.zhihu.com/p/25744686)
1. [使用 mkdocs 搭建个人 wiki 站点](https://blog.csdn.net/u013051748/article/details/108804029)
2. [基于mkdocs-material搭建个人静态博客](https://zhuanlan.zhihu.com/p/56891725)
3. [博客网址增加站点分析](https://jueee.github.io/2020/08/2020-08-09-%E5%8D%9A%E5%AE%A2%E7%BD%91%E5%9D%80%E5%A2%9E%E5%8A%A0%E7%AB%99%E7%82%B9%E5%88%86%E6%9E%90/)
4. [博客添加 Gitalk 评论插件](https://zhuanlan.zhihu.com/p/111846728)
5. [official-mkdocs-material配置指南](https://squidfunk.github.io/mkdocs-material/creating-your-site/#minimal-configuration)
6. [official-mkdocs配置指南](https://www.mkdocs.org/user-guide/configuration/#introduction)
7. [official-mkdocs-wiki-PluginsList](https://github.com/mkdocs/mkdocs/wiki/MkDocs-Plugins)
7. [MkDocs项目文档生成器一](https://blog.csdn.net/KevinDGK/article/details/52388542)
8. [MkDocs项目文档生成器二](https://blog.csdn.net/KevinDGK/article/details/52419819?spm=1001.2014.3001.5502)
9. [laTex支持](https://blog.csdn.net/qq_43094622/article/details/112134442)
`mkdocs build` 
1
该命令创建了一个 site 新目录，可以到项目文件夹中查看，都被保存在了工程名/sit目录下。注意源码被分别输出为 index.html 和 about/index.html.主题中的其他文件也被复制到了 site 目录中。

如果你使用 git 等版本控制系统,，你可能不希望提交构建之后的文档到版本库，在 .gitignore 中添加site/ 即可忽略该目录。

一段时间后，可能有文件被从源码中移除了，但是相关的文档仍残留在 site 目录中。在构建命令中添加--clean 参数即可移除这些文档。

`mkdocs build --clean`

## Discussion
1. [为什么使用mkdocs代替github的wiki做文档管理？](https://www.cnblogs.com/zhaoqingqing/p/9898121.html)

