# 数据分析：世界天气资料库
## 项目简介
本项目演示了如何对数据进行预处理，包括处理缺失值、异常值、以及数据归一化。此外，还涵盖了基本的探索性数据分析（EDA）、预测模型构建以及时间序列分析。

## 文件结构
- `数据清洗及预处理.ipynb`: Jupyter Notebook 文件，包含数据预处理的步骤，具体包括：
  - 读取文件
  - 处理缺失值和异常值
  - 数据归一化
  - 探索性数据分析 (EDA)
  - 预测模型与性能评估
  - 时间序列分析与 LSTM

## 使用方法
1. 克隆或下载该项目。
2. 安装必要的 Python 库：`pandas`、`numpy`、`matplotlib`、`scikit-learn`、`tensorflow` 等。
3. 启动 Jupyter Notebook 环境：
    ```bash
    jupyter notebook
    ```
4. 打开 `数据清洗及预处理.ipynb` 文件，依次执行每个代码单元，完成数据处理、建模和预测分析。

## 依赖
该项目使用以下 Python 库：
- `pandas`: 用于数据处理
- `numpy`: 用于数值计算
- `matplotlib`: 用于可视化
- `scikit-learn`: 用于数据预处理（如归一化等）
- `tensorflow`: 用于 LSTM 时间序列预测

## 项目内容

### 1. 数据读取
使用 `pandas` 读取 CSV 文件，加载数据并进行基本展示。

```python
import pandas as pd
file_path = r"你的文件路径"
data = pd.read_csv(file_path, encoding='utf-8')
data.head()
```
### 2. 处理缺失值和异常值

通过检测数据中的缺失值，并选择合适的方式填补或删除缺失数据。同时，通过箱线图发现并剔除异常值。

```python
missing_data = data.isnull()
missing_count = missing_data.sum()
missing_percentage = (missing_data.sum() / len(data)) * 100
print("每列的缺失值数量:")
missing_count
```
### 3. 数据归一化

使用标准化或归一化方法对数据进行预处理，保证不同特征的数值范围一致。

### 4. 探索性数据分析 (EDA)

通过箱线图、相关性热图等方法对数据进行初步分析，找出潜在的异常值和数据关系。

### 5. 预测模型与性能评估

构建基本的预测模型，并进行性能评估。使用不同的模型评估预测结果。

### 6. 时间序列分析与 LSTM

采用 LSTM 模型对时间序列数据进行预测，展示如何处理时序数据并进行性能评估。

## 数据文件

* 该数据集可在 Kaggle 网站获取。
世界天气资料库：https://www.kaggle.com/datasets/nelgiriyewithana/global-weather-repository/code

## 贡献

如果你想贡献到该项目，请通过 pull request 提交更改，确保代码符合 PEP 8 规范，并附带必要的文档说明。
