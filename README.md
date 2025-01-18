# SEU 人工智能（研讨）课程大作业

## 项目背景

[Kaggle地址](https://www.kaggle.com/competitions/playground-series-s4e2/overview)  

基于给定因素如年龄、性别、饮食习惯和体力活动水平等，预测个体的肥胖风险。参赛者需要运用各种机器学习算法和技术，包括特征选择、模型训练和超参数调整，以提高预测准确性。最终任务是为测试集中每个个体预测其 **`NObeyesdad`** 目标变量的类别值，并按照指定格式提交结果。评估将基于预测结果的准确度进行。

---

## 数据清洗及预处理

### 1. 数据读取初步检查

- 统计了每一列中缺失值的数量。
- 打印了数据框的基本信息以了解各列的数据类型。

### 2. 特征分离

- 将目标变量 **`NObeyesdad`** 从原始数据集中分离出来。

### 3. 特征工程

- **年龄分段**：将年龄分成多个区间。
- **性别编码**：将性别特征由文本形式转换为数值形式。

### 4. 数据预处理

- **数值特征**：通过 `StandardScaler` 进行标准化。
- **分类特征**：使用 `OneHotEncoder` 进行独热编码。

---

## 具体预测方法

### 1. XGBoost 模型

#### 未进行参数调优

![image](https://github.com/user-attachments/assets/2ba5e42f-816e-4f23-a237-f6dd37d36b85)

#### 使用网格搜索（GridSearchCV）进行调优

![image](https://github.com/user-attachments/assets/9453fe43-6771-41df-92da-c2d5132ba499)

#### 使用贝叶斯优化（Hyperopt）进行调优

![image](https://github.com/user-attachments/assets/952e1d81-57c0-4628-be2d-6fae14379733)

---

### 2. LightGBM 模型

#### 通过网格搜索进行调优

![image](https://github.com/user-attachments/assets/29598a88-5747-4545-9440-5f9116d65192)

--- 
