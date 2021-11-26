# 机器学习代码
## 更新于2021.11.26
如何使用我的代码？ 
1. 打开`data.py`，修改第24,25行代码
    ```python
            datapath=".\\data\\train.csv"
            testpath=".\\data\\test.csv"
    ```
    csv文件中，`id`是样本的序列号，`content`是新闻的文本内容。`comment_all`是这个新闻   的所有评论。`label`是新闻真假的标签。其中有3个标签。-1是假新闻，0是不相关，1是真新闻。
    
    若要读取excel格式的文档，修改第`24,25,34,48`行代码即可，但是格式必须相同。
    
    其中`id`是样本的序列号，`content`是新闻的文本内容。`comment_all`是这个新闻的所有评论。`label`是新闻真假的标签。其中有3个标签。-1是假新闻，0是不相关，1是真新闻。

2. 打开`Bert_train.ipynb`或者`NaiveBayes.ipynb`，运行代码即可。



`News_prediction.ipynb`没什么用，本来是用来做数据预处理的，运行之后会生成粗处理后的数据保存，下载时可以忽略。

`data`文件夹中已经包括了初始的数据集和处理之后的数据集。`.csv`文件初始数据集，另外两个是经过`News_prediction.ipynb`代码处理过的。在`Bert`和`NaiveBayes`训练函数中直接加载上来。

`result`文件夹中的文件是朴素贝叶斯和Bert模型训练后的输出文件，准确率分别问87.4和91.1