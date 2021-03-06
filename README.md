# Volatility-Managed Portfolios


## 策略概述

参考Moreira and Muir（2017, JF）构建波动率管理组合（Volatility-Managed Portfolios，VMP），基于2000年到2021年全A股数据展开实证。

针对Liu et al.（2019, JPM）对VMP样本外回测结果的批评，本文测试了VMP的样本外表现，得出不同的结论。

**代码和数据说明**

主要代码为vol-timing.R，主要用到的数据为factor_daily中的因子收益率

参考文献和策略细节详见附件中的pdf。
## 策略原理

![image-20210705153502682](README.assets/image-20210705153502682.png)

![image-20210705153514603](README.assets/image-20210705153514603.png)

![3](README.assets/3.jpg)

![4](README.assets/4.jpg)

## 策略构建

**构建因子池**

![image-20210705153619153](README.assets/image-20210705153619153.png)

因子计算窗口为2000年1月1日到2021年4月1日，计算时剔除金融行业公司、次新股以及ST和ST*股，每月（季）初调仓，调仓时对连续型变量进行上下1%缩尾处理。最后，本文主要计算多头组合日度收益率，多空组合结果类似。个股日度行情数据来自**Tushare**，财务数据来自CSMAR。

**波动率择时**
![5](README.assets/5.jpg)

## 策略表现

### 样本内

![6](README.assets/6.jpg)

### 样本外

![7](README.assets/7.jpg)
