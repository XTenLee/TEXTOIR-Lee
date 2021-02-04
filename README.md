# TEXTOIR HandBook

## :pushpin: What is TEXTOIR
**TEXOIR** is the first integrated and visualized platform for text Open Intent Recognition(OIR). 

We divide OIR into two categories, open intent detection and open intent discovery. Though both of them are both essential modules for OIR, they have different characteristics and implementation methods. However, there is little related work for integrating these two modules. Although some toolkits are developed for Named Entity Recognition, Sentiment Analysis, there is little related work for intent recognition, not even in open-world settings. Therefore, we build a text open intent recognition platform to fill the blank. The demonstration video is available at [there.](https://github.com/XTenLee/TEXTOIR)

## :couple: Audiences

* **Researchers:** With the help of **TEXTOIR**, you can quickly reproduce the open intention recognition models and analyze the effect of the comparison models.
* **New to Open Intent Recognition:** With the help of **TEXTOIR**, you can fully understand the progress in the field of open intent, and process visualization also helps you understand the model in depth.

## :house:  Overview
Our system consists of four parts, which are *Dataset Management*,*Open Intent Detection*, *Open Intent Discovery* and *Data Annotation* respectively. 
* As you can see, *Dataset Management* manages your dataset and you can do some basic operations, such as adding, deleting, modifying and searching.
* With *Open Intent Detection* and *Open Intent Discovery* you can not only manage the new intent detection models but also to train , test models. At the same time, you can analyze the models' effect. 
* We connect the open intent detection and intent discovery modules in a pipeline scheme and achieves multiple model combination. Based on the pipeline scheme, the application of *Data Annotation* is realized.

## :loudspeaker: How to use
![image](https://github.com/XTenLee/TEXTOIR/blob/main/image/handbook.png)
* **Dataset Management:**
数据管理模块存储了当下流行的开放意图识别公开数据集。同样，为了服务于数据标注功能，用户可以在这个模块上传需要标注的数据集。
1. 数据展示
dataset managemnet 展示TEXTOIR中存储的数据集，用户可以通过上方搜索框来筛选感兴趣的数据集。对于数据集的详细信息可以通过”operation“中”Details“查看。
另外，TEXTOIR提供数据修改和数据删除功能。需要注意，用户仅仅被允许删除自己上传的数据集，系统数据集不可修改。
2. 数据增加
TEXTOIR提供数据标签推荐功能，通过”ADD“即可上传本地数据。请注意上传时符合系统规范。

* **Open Intent Detection:**
Open Intent Detection 模块提供了4个基础功能，模型管理、模型训练、模型测试、模型分析。
1. 模型管理：此模块收集了开放意图检测模型的经典baseline和当前sota模型，用户可以查看模型的相关信息。
2. 模型训练：用户可以在此部分查看历史运行记录，以及运行参数。用户可以通过”ADD“训练模型。在训练模型页面，用户可以选择模型、选择数据集以及设置标注比例，已知意图比例。并且根据不同的模型可以设置相对应的训练参数。运行成功后，运行记录页面出现相应的记录。如果用户想中止训练，选择”STOP“即可。
3. 模型测试：此模块展示了模型运行结果。首先，针对单一模型，提供了错误分析功能。根据用户的选择，展示出模型对于每一类意图判断正确和判断错误的结果展示。更进一步的是，详细分析了模型判断错误的结果分析，为改进模型以及发掘意图之间的关系提供了数据支持。
4. 模型分析：此模块利用TEXTOIR提供的样本示例，来可视化分析模型判断的深层原理。对于开放意图检测模型，有两种基本解决思路，基于概率阈值方法和基于决策边界方法。TEXTOIR对这两类模型分别提供了相应的图形化展示。
* **Open Intent Discovery:**
Open Intent Detection 模块提供了4个基础功能，模型存储、模型训练、模型测试、模型分析。
1. 模型
2. 模型训练
3. 模型测试
4. 模型分析
* **Data Annotation:**
Data Annotation 模块提供数据标签推荐功能。此模块集成了新意图检测和新意图发现两个对未标注数据进行标签推荐。
1. 数据准备--在用户端上传
2. 数据标注 -- 选择对应的模型
3. 标签修改 


## :hammer: Install

After updating...

## :question: FAQ

After updating...
  
  
