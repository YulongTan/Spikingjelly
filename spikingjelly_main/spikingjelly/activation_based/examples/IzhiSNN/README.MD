# Izhikevich-SNN (基于 SpikingJelly)

本项目基于 **SpikingJelly** 框架，搭建了 Izhikevich 神经元模型的脉冲神经网络（SNN），并在 **MNIST / 红外行人数据集** 上进行了实验。

---

## 📂 项目结构
```

IzhiSNN/
│── izhi\_fc\_cifar10.py                 # CIFAR-10 全连接 Izhikevich-SNN
│── izhi\_fc\_mnist.py                   # MNIST 全连接 Izhikevich-SNN
│── izhi\_fc\_mnist\_direct\_quantized.py  # MNIST 直接量化版本
│── **init**.py
│
├── Infrared/
│   ├── izhi\_fc\_infrared.py            # 红外数据集 Izhikevich-SNN训练代码文件
│   ├── izhi\_fc\_infrared\_pedestrian\_test.py  # 红外行人检测测试代码文件
│   ├── s\_t\_array.npy                  # 红外数据特征（示例）
│   ├── v\_t\_array.npy                  # 红外数据电压轨迹（示例）
│
└── MNIST/                             # MNIST 数据实验相关（可扩展）

````

---

## 🔧 环境配置

1. 克隆并安装 **SpikingJelly**：
   ```bash
   git clone https://github.com/fangwei123456/spikingjelly.git
   cd spikingjelly
   pip install -e .
````

2. 将本项目文件夹 **IzhiSNN/** 拷贝到：

   ```
   D:\spikingjelly-master\spikingjelly\activation_based\examples\
   ```

3. 安装依赖：

   ```bash
   pip install torch torchvision numpy
   ```

---

## 🚀 使用方法

### 1. 训练 MNIST

```bash
python izhi_fc_mnist.py
```

### 2. 训练红外行人检测

```bash
python Infrared/izhi_fc_infrared.py
```

---

## 📊 功能特点

* 基于 Izhikevich 神经元的4层全连接脉冲神经网络
* 支持 **MNIST / 红外数据集** 分类与行人检测
* 提供 **量化版本** 以支持硬件实现

---

## 📌 参考

* SpikingJelly: [https://github.com/fangwei123456/spikingjelly](https://github.com/fangwei123456/spikingjelly)
* Izhikevich, E. M. "Simple model of spiking neurons." IEEE Transactions on Neural Networks (2003).

