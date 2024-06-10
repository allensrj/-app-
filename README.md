# 自制专有领域词汇表

最近在用不背单词app背单词，里面的词汇书还是四六级高考、雅思托福这种，不过有自制词汇书的选项，于是我想试试用平时工作涉及的文档做一个自制词汇书，以后专门背这里面的单词，或许有助于工作的时候阅读文档。

## 主要思路

1. 把牛津词典的单词取出来；
2. 把我平时工作常用的文档里面的英文单词取出来；
3. 两边一匹配，留下来的英文单词刚好就是app官网里的自制词汇书。

### 涉及细节

1. 我能找到的牛津词典是txt格式，处理后存在一些全大写英文缩写和词缀等解释，没有处理的非常细，后续匹配过程中不符合的自然匹不上。

![image-20240610145031244](/Users/allensrj/Library/Application Support/typora-user-images/image-20240610145031244.png)

2. 同样的涉及我目标领域的比如像sdtmIG等文档，里面也包含一些不是英文单词的东西，同样做了简单的处理，但也没有处理的非常细，后续匹配过程中不符合的自然匹不上。

![image-20240610145302600](/Users/allensrj/Library/Application Support/typora-user-images/image-20240610145302600.png)

## 项目架构

```python
项目文件夹/
├── target        # 存放目标文档的文件夹
├── oxford_dictionary # 存放牛津词典词汇的文件夹
├── function.py      # 功能函数模块
├── main.py          # 主程序执行入口
├── config.py        # 配置文件
├── requirements.txt # 项目依赖文件
```

## 如何运行

把目标文档的pdf格式文件放进target文件夹；

在requirements里面把包装好，在config.py里面填写两个文件夹的路径，然后运行main.py即可。
