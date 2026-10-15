> 历史文字风格示例：来自项目作者的实际报告，保留原稿表达供对照，不是完整或已全面校正的标准答案。原始数据和图表附件不随包分发，不能据此复现实验；数值不得用于其他实验。重复编号、模糊引用、灵敏度命名与估计依据等局限见 [写作规范](writing.md)。新增报告须使用当前数据并遵循 SKILL.md。

# 磁学综合实验报告

## 一、实验数据与处理

### 1. 实验数据记录

如表1,2,3,4

其中数据处理公式有：对称交换法求霍尔电压：$$V_H\approx\frac{V_1-V_2+V_3-V_4}{4}.$$

### 2. 实验一：测量霍尔电压与霍尔电流的关系：

（1）初步观察 $V_H-I_S$ 数据在图表上呈线性分布，对之作最小二乘拟合。令 $V_H=mI_S+b$，则

$$m=\frac{\sum(I_{S,i}-\bar I_S)(V_{H,i}-\bar V_H)}{\sum(I_{S,i}-\bar I_S)^2},\qquad b=\bar V_H-m\bar I_S.$$

代入 $\bar I_S=5.5$ mA、$\bar V_H=6.82725$ mV、$\sum(I_{S,i}-\bar I_S)^2=82.5\ \mathrm{mA^2}$，得到

$$V_H=(1.237833\ \mathrm{mV/mA})I_S+0.019167\ \mathrm{mV},\qquad R^2=0.99998275.$$

如图。

（2）求霍尔灵敏度

螺线管匝数 $N=3200$，取教材标称长度 $L=0.300$ m，以内外径平均值 $D=(30+42)/2=36$ mm 近似等效直径，中心磁场为

$$B_c=\frac{\mu_0NI_M}{\sqrt{L^2+D^2}}
=\frac{(4\pi\times10^{-7}\ \mathrm{T\,m/A})\times3200\times0.500\ \mathrm A}{\sqrt{(0.300\ \mathrm m)^2+(0.036\ \mathrm m)^2}}
=6.654324\ \mathrm{mT}.$$

由 $V_H=K_HI_SB_c$，有

理论K值：$$K_H=\frac{m}{B_c}=\frac{1.237833\ \mathrm{V/A}}{6.654324\times10^{-3}\ \mathrm T}=186.0194\ \mathrm{V/(A\,T)}.$$

### 3. 实验二：测量螺线管中磁感应强度B的大小及分布情况

已知 $$ K_H,V_H,I_s=5mA,I_M=0.5A$$ ,由 $B=V_H/(K_HI_S)$ 逐点换算磁场。如表2。

实验二所求 B-X图表如图2.

### 4. 实验三：亥姆霍兹线圈磁场测量

已知每只圆线圈匝数 $N_h=310$、半径 $R=0.100$ m，理论中心场为

$$B_{\mathrm{th}}(0)=\frac{8\mu_0N_hI_M}{5^{3/2}R}
=\frac{8(4\pi\times10^{-7}\ \mathrm{T\,m/A})\times310\times0.600\ \mathrm A}{5^{3/2}\times0.100\ \mathrm m}
=1.672468\ \mathrm{mT}.$$

同3计算不同X处B，记作$$B_{a+b}$$

$$B_\Sigma^{th}(0)=1.672468\ \mathrm{mT},\qquad
B_{a+b}^{测}(0)=\frac{1.7150\times10^{-3}\ \mathrm V}{186.0194\ \mathrm{V/(A\,T)}\times0.006\ \mathrm A}=1.536578\ \mathrm{mT}.$$

相对偏差为

$$\delta=\frac{B(0)-B_{\mathrm{th}}(0)}{B_{\mathrm{th}}(0)}\times100\%=-8.13\%.$$

### 5. 不确定度估算

（1）单次电压读数及霍尔电压：

$$u_B(V_i)=\frac{0.01}{\sqrt3}\ \mathrm{mV}=0.005774\ \mathrm{mV}.$$

四次读数的该估计分量相互独立时，

$$u_B(V_H)=\frac14\sqrt{\sum_{i=1}^4u_B^2(V_i)}=0.002887\ \mathrm{mV}\approx0.003\ \mathrm{mV}.$$

（2）拟合残差标准差及斜率标准误差：

$$s=\sqrt{\frac{\sum[V_{H,i}-(mI_{S,i}+b)]^2}{10-2}}=0.016511\ \mathrm{mV},$$

$$u(m)=\frac{s}{\sqrt{82.5\ \mathrm{mA^2}}}=0.001818\ \mathrm{mV/mA}.$$

（3）当标定中心场的不确定度为 $u(B_c)$，且输入独立时：

$$\left[\frac{u(B_c)}{B_c}\right]^2=\left[\frac{u(I_M)}{I_M}\right]^2+\left[\frac{L\,u(L)}{L^2+D^2}\right]^2+\left[\frac{D\,u(D)}{L^2+D^2}\right]^2,$$

$$u(K_H)=K_H\sqrt{\left[\frac{u(m)}m\right]^2+\left[\frac{u(B_c)}{B_c}\right]^2}.$$

（4）间接量 $B=V_H/(K_HI_S)$ 的独立输入传播式为

$$u(B)=B\sqrt{\left[\frac{u(V_H)}{V_H}\right]^2+\left[\frac{u(K_H)}{K_H}\right]^2+\left[\frac{u(I_S)}{I_S}\right]^2}.$$

对双线圈中心，仅合成电压读数估计和标定回归贡献：

$$u_{\mathrm{simp}}(B_0)=1.536578\ \mathrm{mT}\sqrt{\left(\frac{0.002887\ \mathrm{mV}}{1.7150\ \mathrm{mV}}\right)^2+\left(\frac{0.2732}{186.0194}\right)^2}
=0.003432\ \mathrm{mT}\approx0.003\ \mathrm{mT}.$$

### 5. 实验结果



## 二、实验结果和讨论

#### 1. 实验结果

霍尔电压与工作电流近似成正比，拟合斜率为1.238 mV/mA；

按教材斜率法求得霍尔灵敏度约186.0 V/(A·T)。

螺线管磁场具有中部近似均匀、端部迅速减弱的分布特征。

亥姆霍兹线圈中心磁场为1.537 mT，简化不确定度为0.003 mT，比理论中心值低8.13%。

#### 2. 分析讨论

四次换向能利用附加电势对电流和磁场的不同奇偶性降低副效应。

双线圈在中心附近形成较平缓分布，向两端逐渐下降。左右位置并非完全对称，±100 mm的换向电压分别为0.9975和1.0900 mV。可能原因包括零点偏移、线圈不共轴、探头偏离轴线或测量期间漂移。

由斜率法标定得到的中心磁场比理想值低约8.13%，标定几何、励磁电流及探头温度或方向变化仍可能带入系统偏差。

