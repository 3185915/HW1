# EuroSAT RGB 图像分类 - 从零实现的全连接神经网络

本项目在 EuroSAT RGB 数据集上，**不使用任何深度学习框架**（如 PyTorch/TensorFlow），仅用 NumPy 从零实现了包含一个隐藏层的全连接神经网络，并完成了超参数搜索、训练、验证、测试以及可视化分析。

## 项目结构
├── sdxxdyczy-eurosatrgb.ipynb # 代码文件
├── error_analysis.png # 错例分析图
├── first_layer_filters.png # 权重可视化图
├── training_curves.png # Loss曲线&Accuracy曲线
└── README.md # 项目说明

## 如何运行
下载github的代码，找到 DATA_PATH 变量，将其改为你的 EuroSAT 数据集实际路径：
DATA_PATH = '/your/path/to/eurosat-rgb/2750'
然后直接运行代码，训练过程会自动进行超参数搜索（网格搜索），然后用最佳超参数在完整训练集上重新训练，最后在测试集上评估并生成可视化结果。

## 预训练模型权重
为了便于复现，我已将训练好的最佳模型权重上传至 Google Drive，链接为：https://drive.google.com/file/d/1PUCxHEfXiT0BOFyttsRmtiD_TG_iz9x5/view?usp=sharing

## 环境依赖

numpy>=1.21.0
scikit-learn>=1.0.0
Pillow>=9.0.0
matplotlib>=3.5.0
tqdm>=4.62.0
