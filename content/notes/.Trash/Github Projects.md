# [[Github Projects]]

## [you-get](https://github.com/soimort/you-get): 
Download videos/pictures/audios from websites


## [Amazon Price Tracker](https://github.com/Den4200/amazon-price-tracker/tree/master/tracker)

## [DecryptLogin](https://github.com/CharlesPikachu/DecryptLogin)
[淘宝商品的数据爬虫](https://mp.weixin.qq.com/s/NhK9eeWNXv_wPnolccRR-g)
[小工具](https://github.com/CharlesPikachu/Tools)
[小游戏](https://github.com/CharlesPikachu/Games)
[AIGames](https://github.com/CharlesPikachu/AIGames)

## [PrettyErrors](https://github.com/onelivesleft/PrettyErrors)
让python报错更加简约

## [GeneralNewsExtractor](https://github.com/kingname/GeneralNewsExtractor)
提取新闻文本 - 可以用来做sentiment
搭配tomd

## [JobFunnel](https://github.com/PaulMcInnis/JobFunnel)
爬取工作列表并保存为csv

## [Peanut](https://github.com/zqqf16/Peanut)
一个静态博客生成工具，由zqqf16.github.com演变而来，目前正在开发中~

## [Humanize](https://github.com/jmoiron/humanize)
This modest package contains various common humanization utilities, like turning a number into a fuzzy human readable duration ("3 minutes ago") or into a human readable size or throughput. 

## [faker](https://github.com/joke2k/faker)
Faker is a Python package that generates fake data for you. Whether you need to bootstrap your database, create good-looking XML documents, fill-in your persistence to stress test it, or anonymize data taken from a production service, Faker is for you.

## [Python-script-converter](https://github.com/ZYunH/Python-script-converter)
这是一个简单的工具，作用是将一个python脚本直接转换为可执行文件(只供mac和Linux系统使用)。如此，你可以在系统的任何地方运行这个脚本。

## [Awesome Python](https://github.com/vinta/awesome-python)
A curated list of awesome Python frameworks, libraries, software and resources.

## [tomd](https://github.com/gaojiuli/tomd)
When crawling online articles such as news, blogs, etc. I want to save them in markdown files but not databases. Tomd has the ability of converting a HTML that converted from markdown. If a HTML can't be described by markdown, tomd can't convert it right. Tomd is a python tool.

## [missingno]
missingno 是一款Python缺失数据的可视化工具。

## [pyecharts]
在Python开发中，提到画图应该十有八九会想到matplotlib，它是一个老牌且强大的绘图库，但是，在使用过程中有一些弊端，例如，不适合离线查看、支持的绘图接口较为单一。

Echarts 是一个由百度开源的数据可视化，凭借着良好的交互性，精巧的图表设计，得到了众多开发者的认可。而 Python 是一门富有表达力的语言，很适合用于数据处理。当数据分析遇上数据可视化时，pyecharts 诞生了。它能够把绘图结果保存为一个html文件，能够动态展示绘图结果，且随时可以打开查看。另外，它支持的绘图类型非常丰富。

## [pyxelate]

pyxelate是一款生成图像像素艺术照的工具，它通过对图像进行下采样，然后结合无监督学习生成调色板合成衣服像素图片。

安装
`pip  install git+https://github.com/sedthh/pyxelate.git`

示例
```from pyxelate import Pyxelate
from skimage import io
import matplotlib.pyplot as plt
img = io.imread("blade_runner.jpg")

height, width, _ = img.shape 
factor = 14
colors = 6
dither = True

p = Pyxelate(height // factor, width // factor, colors, dither)
img_small = p.convert(img)  # convert an image with these settings

_, axes = plt.subplots(1, 2, figsize=(16, 16))
axes[0].imshow(img)
axes[1].imshow(img_small)
plt.show(）
```

## [PySimpleGUI]
顾名思义

## [jieba]
Python 分词库 - 用来句中分词
全模式
```
# encoding=utf-8
import jieba

seg_list = jieba.cut("我来到北京清华大学", cut_all=True)
print("Full Mode: " + "/ ".join(seg_list))  # 全模式

seg_list = jieba.cut("我来到北京清华大学", cut_all=False)
print("Default Mode: " + "/ ".join(seg_list))  # 精确模式

seg_list = jieba.cut("他来到了网易杭研大厦")  # 默认是精确模式
print(", ".join(seg_list))

seg_list = jieba.cut_for_search("小明硕士毕业于中国科学院计算所，后在日本京都大学深造")  # 搜索引擎模式
print(", ".join(seg_list))

【全模式】: 我/ 来到/ 北京/ 清华/ 清华大学/ 华大/ 大学

【精确模式】: 我/ 来到/ 北京/ 清华大学

【新词识别】：他, 来到, 了, 网易, 杭研, 大厦    (此处，“杭研”并没有在词典中，但是也被Viterbi算法识别出来了)

【搜索引擎模式】： 小明, 硕士, 毕业, 于, 中国, 科学, 学院, 科学院, 中国科学院, 计算, 计算所, 后, 在, 日本, 京都, 大学, 日本京都大学, 深造
```

## [MoviewHeavens](https://github.com/lt94/MovieHeavens)
基于Pyqt5的电影天堂电影搜索工具,为了避免找电影期间的各种广告,以及各种页面跳转

## [WechatSougou](https://github.com/Chyroc/WechatSogou)
基于搜狗微信搜索的微信公众号爬虫接口

## [Synonyms](https://github.com/huyingxi/Synonyms)
中文近义词工具包。支持自然语言理解的很多任务：文本对齐、推荐算法、相似度计算、语义偏移、关键字提取、概念提取、自动摘要、搜索引擎等。

## [unimatrix](https://github.com/will8211/unimatrix)
模拟“黑客帝国”影片中的终端动画脚本

## [Scylla](https://github.com/imWildCat/scylla)
一款高质量的免费代理 IP 池工具，仅支持 Python 3.6。

## [TGmeetup](https://github.com/TGmeetup/TGmeetup)
[中文](https://github.com/TGmeetup/TGmeetup/blob/master/documents/README_zh-tw.md)
這是一個搜集與整合技術類社群的專案。我們搜集所有有關於社群的資訊，並透過大家的 Meetup 連結（如：Meetup, KKTIX...），透過 API 拿取最新的活動資訊。讓大家取得社群資訊以及社群的活動資訊的專案。

## [cx-extractor-python](https://github.com/chrislinan/cx-extractor-python)
这是一个对网页正文进行抽取的工具。 cx-extractor 算法的 python 版本，改进了原有算法，使其支持中英文，对新闻类网页正文抽取效果较好

## [weixin_crawler](https://github.com/54xingzhe/weixin_crawler)
基于 Scrapy、Flask、Echarts、Elasticsearch 等实现的微信公众号文章爬虫。自带 UI 界面、分析报告、搜索功能


## [LearnPython](https://github.com/wonderfulsuccess/LearnPython)
以撸代码的形式学习Python, 具体说明在[知乎专栏-撸代码,学知识](https://zhuanlan.zhihu.com/pythoner)
Follow [this guy on github](https://github.com/wonderfulsuccess?tab=repositories)

## [awesome-python-webapp](https://github.com/michaelliao/awesome-python-webapp)
小白的Python入门教程实战篇：网站+iOS App源码→ http://t.cn/zQXcs9S

## [python algorithm](https://github.com/qiwsir/algorithm)
学习python算法-很重要

## [Hitchhiker's Guide to Python](https://github.com/realpython/python-guide)
Topics include:

```Platform and version-specific installations
Py2app, Py2exe, bbfreeze, pyInstaller
Pip
Numpy, scipy, statpy, pyplot, matplotlib
Virtualenv
Fabric
Exhaustive module recommendations, grouped by topic/purpose
Which libraries to use for what
Server configurations & tools for various web frameworks
Documentation: writing it
Testing: Jenkins & tox guides
How to easily interface hg from git
```

## [incubator-superset](https://github.com/apache/incubator-superset)
企业级的数据探索、展示平台。功能很强大，可以用来做数据分析、展示。

 
## [textfilter](https://github.com/observerss/textfilter)
基于某 1w 词敏感词库，用 Python 实现几种不同的过滤方式。用于过滤敏感词的实用模块

## [qrcode](https://github.com/sylnsfar/qrcode)
Python 写的生成动态、彩色、各式各样的二维码，详细的中文文档

## [httpie](https://hellogithub.com/periodical/statistics/click/?target=https://github.com/jkbrzt/httpie)
非常好用的命令行 HTTP 客户端，cURL 的替代者，返回的结果支持高亮，提高了可读性。用于调试接口、查看服务器返回的 HTTP 协议的信息。[Doc](https://httpie.org/docs#examples)

## [fake-useragent](https://github.com/hellysmile/fake-useragent)
伪装浏览器身份，常用于爬虫。这个项目的代码很少，可以阅读一下，看看 ua.random 是如何返回随机的浏览器身份的 

## [ngrok](https://github.com/inconshreveable/ngrok)
一个十分方便、好用的内网穿透工具，它可以把本地某个端口的服务，通过一个安全隧道，映射到公网的一个地址。同时它提供了一个 Web 页面，展示了每个请求、响应的所有信息，便于调试本地的程序。基本的使用方法如下：
```
ngrok 协议 本地服务监听的端口
ngrok http 8000

创建成功会返回公网地址，然后通过该地址就可以访问到本地的服务。
本地访问 http://localhost:4040，就可以查看关于每个请求、响应的相关数据
```

## [glances](https://github.com/nicolargo/glances)
一个可以让你一目了然你的系统情况（类 (h)top）的工具，它界面友好，安装方便：pip install glances

## [saythanks.io](https://hellogithub.com/periodical/statistics/click/?target=https://github.com/kennethreitz/saythanks.io)
Kennethreitz 写的一个简单的网站（基于 Flask），用于向开源项目作者发送感谢邮件的 Web App。该项目结构简单，可以用来学习大神是如何快速开发 Web 项目、方法、代码风格、开发常用库。而且该项目的意义也特别好：感谢开源项目的作者，愿开源社区越来越好，网站地址

## [certbot](https://github.com/certbot/certbot)
免费的自动启用和部署 HTTPS 的工具，让你的网站开启 HTTPS 变得简单快捷。在部署教程页面选择服务器的操作系统和 Web 服务器，之后根据给出的步骤一步步的执行命令就行了，[部署教程](https://certbot.eff.org)

## [musicbox](https://github.com/darknessomi/musicbox)
基于 Python 编写的网易云音乐命令行版本，使用起来简单优雅，能够快速安装及使用

## [django-blog-tutorial](https://github.com/HelloGitHub-Team/HelloDjango-blog-tutorial)
基于最新版 Django 1.10 和 Python 3.5，通过 26 篇教程一步步带你使用 Django 从零开发一个个人博客系统，在实践的同时掌握 Django 的开发技巧
[博客教程](https://www.zmrenwu.com/courses/hellodjango-blog-tutorial/)

## [3y](https://github.com/ZhongFuCheng3y/3y)
📓从Java基础、JavaWeb基础到常用的框架再到面试题都有完整的教程，几乎涵盖了Java后端必备的知识点

## [ Stock Market Sentiment Analysis](https://github.com/algosenses/Stock_Market_Sentiment_Analysis)
股市情感分析

## [stocksight](https://github.com/shirosaidev/stocksight#how-to-use)

Stock market analyzer and stock predictor using Elasticsearch, Twitter, News headlines and Python natural language processing and sentiment analysis. How much do emotions on Twitter and news headlines affect a stock's price? Let's find out...

## [Awesome-Quant-Machine-Learning-Trading](https://github.com/grananqvist/Awesome-Quant-Machine-Learning-Trading)

Quant/Algorithm trading resources with an emphasis on Machine Learning.

## [EastMoneySpider](https://github.com/algosenses/EastMoneySpider)
东方财富网股吧爬虫
















And because porn sites throttle the download speed, it's nice that you can use external downloaders to use multiple connections:
youtube-dl --external-downloader axel --external-downloader-args "-n 10 -a"




















