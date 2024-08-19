# 1 **模型量化是什么，有何用**

# 2 **什么情况下我们可以使用模型量化**


# 3 **模型量化的常用方法以及其优缺点**

## 3.1 浮点模型转换成量化模型的方法

#### 3.1.1 data free 
不使用校准集，传统的方法直接将浮点参数转化成量化数，使用上简单，但是一般会带来很大的精度损失
#### 3.1.2 calibration
基于校准集方案，通过输入少量真实数据进行统计分析

## 3.2 模型量化的两种方法 PTQ and QAT

![[Pasted image 20240819115949.png]]
#### 3.2.1 Post-trining quantization (PTQ):

#### 3.2.2 Quantization-Aware Training (QAT):

# 参考资料：
https://zhuanlan.zhihu.com/p/505570612
https://www.youtube.com/watch?v=kw7S-3s50uk
https://developer.horizon.ai/api/v1/fileData/horizon_j5_open_explorer_cn_doc/oe_mapper/source/faststart/ptq_qat_overview.html
https://symbl.ai/developers/blog/a-guide-to-quantization-in-llms/