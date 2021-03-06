#兮兮（Xixi） -- a cute girl using Python with AIML

## 概述
兮兮是一个用Python实现的小伙伴。
她能撒娇卖萌，她能成为你忠实的小秘书，她能陪你聊天为你唱歌给你读书读新闻。
如果她不乖的话，你还可以调教她。

## NOTE
1. 播放音乐


## 目录说明
	\Docs	一些参考文档
	\Source	源代码
		\XiXiServer	兮兮的core。直接python Xixi.py即可使用
		\gargets	让兮兮做一些事的小工具，可以单独使用
	\Img	一些截图信息
	FAQ.md	开发过程中遇到的问题记录
	README.md
	

## 修改日志
* 2015.08.18   初步完成兮兮一问一答形式。使用jieba进行分词，aiml文件中的项以空格隔开。并可以根据在某个特定的模式下调用脚本播放豆瓣音乐。但是分词性能不高。

* 2015.08.21 jieba分词性能不高。匹配中文需要将中文句子字与字之间隔开，尝试自己编写，结果还是搞不定。暂时使用github上的，专注主要内容的实现。有时间再尝试。

* 2015.08.22 不纠结于自己造轮子果然惬意多了。当前实现了如果跟兮兮说无聊了，兮兮会给你播放豆瓣音乐的问题。但是还是没解决兮兮先回复一句话再放音乐的问题……
![](/Img/20150822.PNG)

* 2015.08.23 给兮兮添加了博客阅读（简书/每日一文）的功能。使用了百度语音合成。但是还是没有想好入口点。另外，语速有点快，调节没感觉到明显的效果.

* 2015.08.24 调用SIMSIM接口。如果问题在语料中找不到答案，则到SIMSIM查询，并把答案保存。

* 2015.09.13 新增自动打卡的garget。目前只能支持百度贴吧打卡，用户信息需要在user_config.ini中配置。使用mpg123播放语音的时候，mpg123自身的提示信息其实木有啥用处，因此将所有需要使用mpg123播放语音的garget都改成运行时不显示mpg123的信息。自动学习功能还是有点问题，总觉得不够完美呢

## 环境信息
1. aiml for python

		pip install aiml

2. jieba

		pip install jieba
		
3. banana pro一块


## TO-DO
1. 闹钟
2. 日程提醒
3. 晨间新闻（60sss）
4. 中文语料：要不从各种小言中抓取统计弄出来吧？
5. 博客阅读（简书/每日一文）
6. android客户端
7. 自动学习功能
8. 打卡（就是一键式自动到百度知道之类的上面打卡签到）
9. 涨知识（例如复习IT知识点呀）
10. 通过互联网进行自动学习和获取知识



## 参考
1. https://github.com/andelf/PyAIML
2. [让机器人模块 PyAIML 平滑处理中文](http://pythonic.zoomquiet.io/data/20070709214730/index.html)

