# 机器学习代码
`data.py`函数可以对csv格式的文件进行处理，格式如下：
```python
    dataset=pd.read_csv("train.csv")
    dataset.columns=['id','content','comment_all','label']
    dataset=dataset.set_index('id')
    test=pd.read_csv("test.csv")
    test.columns=['id','content','comment_all']
    test=test.set_index('id')
    testset=test
```
其中`id`是样本的序列号，`content`是新闻的文本内容。`comment_all`是这个新闻的所有评论。`label`是新闻真假的标签。其中有3个标签。-1是假新闻，0是不相关，1是真新闻。
`News_prediction.ipynb`没什么用，本来是用来做数据预处理的，运行之后会生成粗处理后的数据保存，下载时可以忽略。
`data`文件夹中已经包括了初始的数据集和处理之后的数据集。`.csv`文件时初始数据集，另外两个是经过`News_prediction.ipynb`代码处理过的。在`Bert`和`NaiveBayes`训练函数中直接加载上来。