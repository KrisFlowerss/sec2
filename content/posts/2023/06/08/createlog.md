---
title: 建站历程
date: 2023-06-08
Categories:
- 杂项
Tags:
- 总结
- 历程
- Hugo
---

## 初衷

&emsp;&emsp;很早就想要弄个人博客了，中间有一段时间有事导致计划被闲置了，只是申请了一个免费域名并解析在Cloudflare。现在有空就把这个计划重置了。

&emsp;&emsp;由于我想要尝试的必须是可以在Vercel能够部署的，所以我的选择挺有限的，刚开始尝试了很多其他架构的博客，比如刚开始尝试的jekyll架构的博客，却发现更改背景无果，我想着总不可能用初始模版搭建就完事了吧，黑白的文字和初始样式也太难看了，于是这个架构被我抛弃了，后面又试了Hexo架构，发现还是有很多不满意的地方。

## 开始尝试

&emsp;&emsp;于是我最后忍不了了，问了ChatGpt说：“哪个架构的个人博客比较适合小白？”他很肯定地给了我唯一的答案：Hugo的架构是最适合的。于是我开始找能够在Vercel部署的Hugo模版，有点比较难找，但还是给我找到了唯一一个[大佬配置好的](https://github.com/Fintinger/hugo-auto-deploy)能用的比较满意的。  非常推荐,还有[他自己的博客网站]([blog.archai.site/](https://blog.archai.site/))。我配置好的网站首页在页脚也标注了。非常感谢🙏。

&emsp;&emsp;刚开始直接fork完用vercel部署是没有用的，会显示错误，这是我遇到的**第一个问题**，具体错误详情我也不想找了，最后了解到需要在原文件根目录下创建一个vercel.json文件，详情如下：

```json
{
    "build": {
      "env": {
        "HUGO_VERSION": "xxx"//xxx最好为你本地使用的hugo版本号
      }
    }
  }
  
```

​	&emsp;&emsp;OK，接下来就是把作者的一些相关博客和页面的喜好设置更改就行了。看着作者的视频背景好看的不行，我也找了一个，感觉很适合做视频背景，如你所见，现在用电脑端点击首页就可以看见了。于是就去弄图床，去用Gitee+PicGo做图床，图床很成功，但是视频好像就有问题了，当时没用F12检查是什么样的错误，于是就加了原作者的微信。他告诉我他的视频床是用阿里云oss存储的，于是也去开通了阿里云的oss存储，将跨域规则添加了一个*并成功地解决了问题。

## 末尾

&emsp;&emsp;现在博客已经开始正常使用，后面再写一个熟悉MarkDown编辑的博客以熟悉博客的基本编写功能。


<div align=center><img src="https://imagebedss.oss-cn-shenzhen.aliyuncs.com/2245a04c50234527abd255a47f5fdbeb.gif"  />