# Dataset Interview – Slides README

## 目标

在 dataset interview 中，slides 的目标不是展示“最强模型”，而是呈现一个**结构清晰、判断合理、可复现、可解释**的研究流程。Slides 等价于一篇 mini research note。

---

## Slides 总体结构（10–12 页）

### 1. Problem Framing

* 数据类型（time series / regression / classification）
* 任务的一句话定义
* 核心挑战（如非平稳性、噪声、样本有限等）

---

### 2. Data Overview

* 样本量、时间跨度
* 特征数 / target
* 缺失值与异常值概况
* 时间结构（是否均匀、是否存在 gaps）

---

### 3. EDA – 核心发现

* Target 分布特征（heavy tail / shift / skewness）
* 时间维度上的趋势、季节性或 regime change
* 特征与 target 的主要相关结构
* 对建模假设的直接影响

---

### 4. Problem Decomposition

* Train / validation / test 的划分逻辑（是否 time-aware）
* 建模流程拆解：baseline → 特征 → 模型 → 验证
* 明确未采用方案及原因（如数据泄露、假设不成立）

---

### 5. Baseline Model

* 简单 baseline（mean / linear / ridge / naive forecast）
* Baseline 指标
* Baseline 的失效模式（underfit / bias）

---

### 6. Feature Engineering

* Lag / rolling / difference 等时间特征（如适用）
* 标准化、去趋势等预处理
* 类别特征处理方式（如存在）
* 明确特征构造中的信息边界

---

### 7. Models Tried & Rationale

* 尝试的模型列表
* 每个模型的引入理由
* 主要优缺点与风险（稳定性、过拟合、可解释性）

---

### 8. Validation & Metrics

* 验证策略（时间切分 / rolling validation 等）
* 指标选择理由
* 训练–验证差异与稳定性判断

---

### 9. Final Model & Results

* 最终模型说明
* 核心指标
* 与 baseline 的对比

---

### 10. Interpretability & Sanity Checks

* Feature importance / 系数分析
* 残差行为与极端样本检查
* 数据泄露与异常行为排查

---

### 11. Limitations & Next Steps

* 数据层面的限制
* 模型假设不满足之处
* 在更多时间或数据条件下的改进方向

---

## 核心原则

* 先理解数据，再选择模型
* Baseline 是必要参照
* Validation 优先于模型复杂度
* 稳定性与可解释性优先于峰值指标
* 明确假设、边界与 trade-off

---

## 本仓库内容说明

* `README.md`：Slides 结构与逻辑说明（本文档）
* `cheatsheet.ipynb`：常用 EDA / 特征工程 / 建模代码模板
* `slides/`：最终展示用 PPT（如适用）

---

## 使用说明

该 README 作为 dataset interview 的统一结构约束，用于保证分析流程完整、表达一致、结论可解释。
