#### single_video_model

基于搜狐单视频数据的推荐模型。

- 文档结构如下：

  G:.
  │  main.py			# 主函数，加载数据、模型，训练保存并评估。
  │  tf1.15.yaml
  │
  ├─bin
  ├─configs
  │  │  config.py		# 参数设定
  │  │  __init__.py
  │  │
  │  └─__pycache__
  │          config.cpython-36.pyc
  │          __init__.cpython-36.pyc
  │
  ├─dataset
  │      part-00002.csv
  │
  ├─demos
  │      modeldemo.py
  │
  ├─doc
  │  │  adulttest.py
  │  │  dataloader.py	# 加载**单视频特征**格式数据。
  │  │  evaluate.py		# 包含模型的评估函数。
  │  │  single_video_letor.py		# 特征工程，根据日志生成**单视频特征**
  │  │  tensorboard.py	# 模型的可视化。
  │  │  __init__.py
  │  │
  │  └─__pycache__
  │          dataloader.cpython-36.pyc
  │          evaluate.cpython-36.pyc
  │          __init__.cpython-36.pyc
  │
  ├─models		# 加载模型的代码
  │  │  DeepFM.py
  │  │  WDmodel.py	# Wide and Deep 模型
  │  │  __init__.py
  │  │
  │  └─__pycache__
  │          WDmodel.cpython-36.pyc
  │          __init__.cpython-36.pyc
  │
  └─model_h5_t1.15.0_k2.2.4-tf		#保存训练好的模型的文件夹，模型命名格式为：模型-时间(月-日-小时-分钟)

  ​        deep-07-14-14-24.h5
  ​        deep-07-14-14-33.h5
  ​        deep-07-14-15-07.h5
  ​        deep-07-14-16-31.h5
  ​        model-07-13-12-23.h5
  ​        model-07-14-11-37.h5
  ​        model-07-14-12-01.h5
  ​        model-07-14-12-12.h5
  ​        model_log.txt	# 模型日志，包含模型结构，评估结果，实验信息。
  ​        wide-07-14-14-16.h5
  ​        wide-07-14-16-48.h5
  ​        widedeep-07-20-17-35.h5
  ​        widedeep-07-20-17-43.h5
  ​        widedeep-07-20-17-53.h5
  ​        widedeep-07-20-17-58.h5
  ​        widedeep-07-20-18-16.h5
  ​        widedeep-07-20-18-27.h5
  ​        widedeep-07-20-18-38.h5
  ​        widedeep-07-20-18-46.h5
  ​        widedeep-08-03-15-04.h5

- 环境加载：

  - python==3.6.10

    tensorflow==1.15

    numpy==1.19

  - 使用anaconda搭建环境，具体环境和依赖包保存在tf1.15.yaml文件中，conda重建环境指令如下：

    conda env create -f tf1.15.yaml 

