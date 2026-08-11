---
title: '无穷小的比较'
description: '无穷小的比较是在同一极限过程中，通过两个无穷小比值的极限，判断它们趋于 0 的快慢：比值为 0 是高阶无穷小，趋于 0 更快；比值无穷大为低阶无穷小，趋于 0 更慢；比值为非零常数是同阶无穷小；比值为 1 则为等价无穷小，等价无穷小可简化乘除极限，一般不能用于加减替换。'
pubDate: 1996-01-01 02:04:01
tags: [极限]
categories: [专转本]
heroImage: ./infinitesimal_difference.png
heroImageAlt: '无穷小差值，借助放大镜展示无穷小间隔，直观说明 0.999 无限循环等于 1。'
---

无穷小的比较是指在同一极限过程中，通过计算两个无穷小量之比的极限，来衡量它们趋近于零的**相对速度**。

设在同一极限过程（如 $x \to x_0$ 或 $x \to \infty$）中，$\alpha(x)$ 与 $\beta(x)$ 均为无穷小量，且 $\alpha(x) \neq 0$。记它们的比值极限为：

$$L = \lim \frac{\beta(x)}{\alpha(x)}$$

## 相对阶数分类

根据极限 $L$ 的结果，无穷小之间的关系分为以下几类：

1. **高阶无穷小**：若 $L = 0$，称 $\beta$ 是比 $\alpha$ 更高阶的无穷小，记作 $\beta = o(\alpha)$。说明 $\beta$ 趋于 0 的速度比 $\alpha$ 更快。
2. **低阶无穷小**：若 $L = \infty$，称 $\beta$ 是比 $\alpha$ 更低阶的无穷小。说明 $\beta$ 趋于 0 的速度比 $\alpha$ 更慢。
3. **同阶无穷小**：若 $L = C \neq 0$（$C$ 为常数），称 $\beta$ 与 $\alpha$ 是同阶无穷小，说明两者趋于 0 的速度处于同一数量级。
4. **等价无穷小**：若 $L = 1$，称 $\beta$ 与 $\alpha$ 是等价无穷小，记作 $\alpha \sim \beta$。

## 当 $x \to 0$ 时的常用等价无穷小

在极限制算中，熟记常见的等价无穷小可以大幅简化计算：

- $\sin x \sim x$
- $\tan x \sim x$
- $\arcsin x \sim x$
- $\arctan x \sim x$
- $e^x - 1 \sim x$
- $\ln(1+x) \sim x$
- $a^x - 1 \sim x \ln a \quad (a > 0, a \neq 1)$
- $1 - \cos x \sim \frac{1}{2}x^2$
- $(1+x)^a - 1 \sim ax$

## 等价无穷小代换定理及运算法则

**代换定理**：若在同一极限过程中，$\alpha \sim \alpha'$ 且 $\beta \sim \beta'$，且 $\lim \frac{\alpha'}{\beta'}$ 存在，则：

$$\lim \frac{\alpha}{\beta} = \lim \frac{\alpha'}{\beta'}$$

**计算时的注意事项**：

- **乘除法因子可直接代换**：当无穷小量作为整个分子或分母的乘积/商的因子时，可以直接替换。

  例如：$\lim_{x \to 0} \frac{\sin 2x}{\ln(1+3x)} = \lim_{x \to 0} \frac{2x}{3x} = \frac{2}{3}$

- **加减法项不可随意代换**：若无穷小处于加减运算法则中（如 $\alpha - \beta$），直接用等价无穷小替换可能会导致最高阶项抵消，从而得出错误结论。加减法的无穷小处理通常需改用泰勒公式（Taylor Series）展开到足够高阶项后再计算。
