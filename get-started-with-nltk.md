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

