# Maupassant
Maupassant theme, ported to Hugo.

预览效果:[胡刘郏的技术博客](http://www.huliujia.com)

一款非常简洁、性能高的Hugo主题，适配不同的设备（PC，Mobile等）。

当前主题fork 自 [flysnow](https://github.com/flysnow/maupassant-hugo) ，绝大部分特性来自于flysnow，本人根据个人喜好做了一些定制。来自flysnow的特性请看[flysnow README](README_flysnow.md)

基本配置

```toml
baseURL = "https://www.huliujia.com/"
languageCode = "zh-cn"
title = "胡刘郏的技术博客"
theme = "maupassant"
summaryLength = 128
hasCJKLanguage = true
preserveTaxonomyNames = true

[author]
    name = "胡刘郏"

[params]
    author = "胡刘郏"
    subtitle = "Stay hungry. Stay foolish."
    keywords = "linux,C++,C,后台开发,操作系统,数据结构,算法,计算机网络"
    description = ""
    recentPost = fals
```

# 本分支定制功能

## 可以选择是否显示最近发表的文章，

显示最近文章：将params.recentPost的值修改为true

```toml
[params]
    recentPost = true
```

不显示最近文章：将params.recentPost的值修改为false，或者直接删除recentPost域

```toml
[params]
    recentPost = false
```

## 可以选择是否显示不蒜子页面计数器的计数值

如果要启用不蒜子计数器，在config.toml中添加如下配置：

```toml
[params.busuanzi]
  rocord = true
  show = true
```

如果只想记录，不想在页面中显示，可以将show的值改为false：

```toml
[params.busuanzi]
  rocord = true
  show = false
```

## 版权声明支持（在文章底部显示）

如果要启用版权声明，在config.toml中添加如下配置

```toml
[params.cc]
    name = "知识共享署名-非商业性使用-禁止演绎 4.0 国际许可协议"
    link = "https://creativecommons.org/licenses/by-nc-nd/4.0/deed.zh"
    types = ["blog","posts"]
```

types指定了添加版权声明的文章类型，可以添加多个。文件类型就是你在content下的子目录名字。不在types中的文章底部不会显示版权声明

可以直接将上面的代码复制粘贴到config.toml中，也可以根据需要前往官网https://creativecommons.org选择合适自己的许可协议，然后替换name和link的内容即可。

## 其他定制内容

将订阅栏放在了侧边栏最上部，简化了RSS显示