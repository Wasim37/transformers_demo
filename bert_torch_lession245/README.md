<!--
 * @Author: your name
 * @Date: 2021-08-28 10:27:02
 * @LastEditTime: 2021-08-31 10:28:25
 * @LastEditors: your name
 * @Description: In User Settings Edit
 * @FilePath: \wasim_bert\bert_torch_lession245\README.md
-->


## 代码结构
代码分为 6 个部分：main.py，model.py，prepro.py，parser_args.py，src 文件夹以及 shell 脚本文件。

- main.py：主函数入口文件，包括模型的训练和验证流程，模型加载、模型保存、模型输出，控制日志输出等。
- model.py：模型定义模块，即定义模型计算图，负责定义模型从输入到输出（loss, logits）的处理流程。
- prepro.py：数据处理模块，负责将文本序列的句子处理成模型需要的 tensor，包括不同任务的 processor 预处理函数。
- parser_args.py：统一设置超参数的文件。
- src ：transfomers 库的源代码文件，包括已经封装好的各种模型类，配置类，我们这一节课程不涉及这里的代码。
- 脚本文件：train.sh，eval.sh。训练和测试的脚本文件，可一键运行。
- ner_prep.py：NER 任务的数据预处理脚本。


## 数据集
当前目录新建chinese_wwm_pytorch和data文件夹，存放预训练模型文件和数据集。

- 分类数据集：中文情感分析数据集 ChnSentiCorp

  下载链接：https://bj.bcebos.com/paddlehub-dataset/chnsenticorp.tar.gz

- 匹配数据集：哈工大语义相似度数据集 LCQMC

  下载链接：https://bj.bcebos.com/paddlehub-dataset/lcqmc.tar.gz

- 序列标注数据集：中文微博命名实体识别数据集 weiboNer

  下载链接：https://github.com/quincyliang/nlp-public-dataset/tree/master/ner-data/weibo


## 训练与评估

训练：
```
task_output_name是本次训练任务的输出路径
sh train.sh <task_output_name>
```


评估：
```
task_output_name是本次训练任务的输出路径
sh eval.sh <task_output_name>
```

