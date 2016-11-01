安装nltk包,并下载book数据\(`from nltk.book import *`\)

##### 1.文本搜索

**函数**`concordance(some word)` :在文本中搜索包括某个单词的句子,包括前后文,以搜索的单词为中心对齐,按行显示排列.

> `from nltk.book import *`
> `text1.concordance("monstrous")`

**函数**`similar(some word)`:寻找相似的用法或者单词

**函数**`common_context([])`允许我们同时探索两个或以上单词的上下文

**函数**`dispersion_plot([])`用离散图表示单词在整个文本中的位置,每个竖线代表每个单词的位置,每行代表整个文本

**函数**`generate`生成随机文本

##### 2.词汇统计

文本长度 `len(text)`

文本中的标识符\(单词和标点\)个数`len(set(text))` \(用`set`获得词汇表\)

`sorted(set(text))`排序的词汇表

计算平均每个单词被使用的次数

> `from future import division`
> `len(text)/len(set(text))`

在nltk中有特定的函数去统计词汇

函数`count(word)` 计算某个单词在文中出现的次数

##### 3.频率分布

函数`FreqDist(text)`生成`单词:频率`字典
函数`hapaxes()`查看低频词
函数`most_common(n)`查看前n个高频词

| 函数名 | 功能 |
| --- | --- |
| `fdist =FreqDist(samples)` | 创建包含给定样本的频率分布 |
| `fdist.inc(sample)` | 增加样本 |
| `fdist['monstrous']` | 计算给定样本出现的次数 |
| `fdist.freq('monstrous')` | 给定样本的频率 |
| `fdist.N()` | 样本总数 |
| `fdist.keys()` | 以频率递减次序排列的样本列表 |
| `for ... in fdist` | 以频率递减次序遍历列表 |
| `fdist.max()` | 数值最大的样本 |
| `fdist.tabulate()` | 绘制频率分布表 |
| `fdist.plot()` | 绘制频率分布图 |
| `fdist.plot(n,cimulative=True)` | 绘制累积频率分布图 |
| `fdist1<fdist2` | 测试样本在fdist1中出现的频率是否小于在fdist2中出现的频率 |

##### 4.细粒度的选择词
短高频词    长低频词

##### 5.词语搭配和双连词(bigrams)
| 函数名 | 功能 |
| --- | --- |
| `bigrams([])` | 列出出现在一块儿的词组 |
| `text.collocations()` | 频繁出现的词组(双连词) |



