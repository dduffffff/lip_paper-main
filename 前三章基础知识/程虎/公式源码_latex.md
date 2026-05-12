程虎论文前三章公式源码 LaTeX 版

说明：
- 以下内容依据 PDF 提取结果整理为 LaTeX，可直接复制到论文或笔记中使用。
- 公式 (2.43)、(2.44)、(2.63) 到 (2.82) 含复杂矩阵或 OCR 残缺，已尽量还原，但仍建议对照原 PDF 做最终校对。

公式 (2.1) | PDF page 27
```latex
\mathbf{T}_{01} =
\begin{bmatrix}
1 & 0 & 0 & 0 \\
0 & \cos q_1 & -\sin q_1 & 0 \\
0 & \sin q_1 & \cos q_1 & 0 \\
0 & 0 & 0 & 1
\end{bmatrix}
```

公式 (2.2) | PDF page 27
```latex
\mathbf{T}_{12} =
\begin{bmatrix}
\cos q_2 & 0 & \sin q_2 & 0 \\
0 & 1 & 0 & 0 \\
-\sin q_2 & 0 & \cos q_2 & 0 \\
0 & 0 & 0 & 1
\end{bmatrix}
```

公式 (2.3) | PDF page 27
```latex
\mathbf{T}_{23} =
\begin{bmatrix}
\cos q_3 & 0 & \sin q_3 & 0 \\
0 & 1 & 0 & l_1 \\
-\sin q_3 & 0 & \cos q_3 & 0 \\
0 & 0 & 0 & 1
\end{bmatrix}
```

公式 (2.4) | PDF page 27
```latex
l_1 =
\begin{cases}
l_{abad}, & \text{左前腿、左后腿}, \\
-l_{abad}, & \text{右前腿、右后腿},
\end{cases}
\qquad
l_2 = -l_{hip}
```

公式 (2.5) | PDF page 27
```latex
\mathbf{p}_3 =
\begin{bmatrix}
0 \\
0 \\
l_3 \\
1
\end{bmatrix},
\qquad
l_3 = -l_{knee}
```

公式 (2.6) | PDF page 28
```latex
\mathbf{p}_0 = \mathbf{T}_{01}\mathbf{T}_{12}\mathbf{T}_{23}\mathbf{p}_3
```

公式 (2.7) | PDF page 28
```latex
\begin{bmatrix}
x_p \\
y_p \\
z_p
\end{bmatrix}
=
\begin{bmatrix}
l_3 \sin(q_2 + q_3) + l_2 \sin q_2 \\
-l_3 \sin q_1 \cos(q_2 + q_3) + l_1 \cos q_1 - l_2 \cos q_2 \sin q_1 \\
-l_3 \cos(q_2 + q_3) - l_2 \cos q_2
\end{bmatrix}
```

公式 (2.8) | PDF page 28
```latex
\delta y_p = \frac{\partial y_p}{\partial q_1}\,\delta q_1 + \frac{\partial y_p}{\partial q_2}\,\delta q_2 + \frac{\partial y_p}{\partial q_3}\,\delta q_3
```

公式 (2.9) | PDF page 28
```latex
\delta z_p = \left(-l_2 \cos q_1 \sin q_2 - l_3 \cos q_1 \sin(q_2 + q_3)\right)\delta q_2 + \left(-l_3 \cos q_1 \sin(q_2 + q_3)\right)\delta q_3
```

公式 (2.10) | PDF page 28
```latex
\begin{bmatrix}
\dot{x}_p \\
\dot{y}_p \\
\dot{z}_p
\end{bmatrix}
=
\begin{bmatrix}
J_{11} & J_{12} & J_{13} \\
J_{21} & J_{22} & J_{23} \\
J_{31} & J_{32} & J_{33}
\end{bmatrix}
\begin{bmatrix}
\dot{q}_1 \\
\dot{q}_2 \\
\dot{q}_3
\end{bmatrix}
= \mathbf{J}
\begin{bmatrix}
\dot{q}_1 \\
\dot{q}_2 \\
\dot{q}_3
\end{bmatrix}
```

公式 (2.11) | PDF page 29
```latex
\mathbf{J}(\theta) =
\begin{bmatrix}
0 & c_{23} l_3 + c_2 l_2 & c_{23} l_3 \\
-s_1 l_1 - c_1 c_2 l_2 - c_1 c_{23} l_3 & s_1 s_2 l_2 + s_1 s_{23} l_3 & s_1 s_{23} l_3 \\
c_1 l_1 + s_1 c_2 l_2 + s_1 c_{23} l_3 & c_1 s_2 l_2 + c_1 s_{23} l_3 & c_1 s_{23} l_3
\end{bmatrix}
```

公式 (2.12) | PDF page 29
```latex
\begin{bmatrix}
\dot{q}_1 \\
\dot{q}_2 \\
\dot{q}_3
\end{bmatrix}
= \mathbf{J}^{-1}
\begin{bmatrix}
\dot{x}_p \\
\dot{y}_p \\
\dot{z}_p
\end{bmatrix}
```

公式 (2.13) | PDF page 29
```latex
\boldsymbol{\tau}^{\mathrm{T}}\delta \mathbf{q} + (-\mathbf{F})^{\mathrm{T}}\delta \mathbf{p}^{0} = 0
```

公式 (2.14) | PDF page 29
```latex
\boldsymbol{\tau} = \mathbf{J}^{\mathrm{T}}\mathbf{F}
```

公式 (2.15) | PDF page 29
```latex
\begin{bmatrix}
y_p \\
z_p
\end{bmatrix}
=
\begin{bmatrix}
\cos q_1 & -\sin q_1 \\
\sin q_1 & \cos q_1
\end{bmatrix}
\begin{bmatrix}
l_1 \\
-L
\end{bmatrix}
```

公式 (2.16) | PDF page 29
```latex
\begin{cases}
y_p = l_1 \cos q_1 + L \sin q_1, \\
z_p = l_1 \sin q_1 - L \cos q_1,
\end{cases}
\Rightarrow
\begin{cases}
y_p = l_1 + L \tan q_1, \\
z_p = l_1 \tan q_1 - L.
\end{cases}
```

公式 (2.17) | PDF page 30
```latex
\frac{y_p}{z_p} = \frac{l_1 + L \tan q_1}{l_1 \tan q_1 - L}
```

公式 (2.18) | PDF page 30
```latex
\tan q_1 = \frac{z_p l_1 + y_p L}{y_p l_1 - z_p L}
```

公式 (2.19) | PDF page 30
```latex
q_1 = \operatorname{atan2}(z_p l_1 + y_p L,\, y_p l_1 - z_p L)
```

公式 (2.20) | PDF page 30
```latex
\angle O_2 O_3 P = \arccos\left(
\frac{\lVert \overrightarrow{O_3 O_2} \rVert^2 + \lVert \overrightarrow{O_3 P} \rVert^2 - \lVert \overrightarrow{O_2 P} \rVert^2}{2\lVert \overrightarrow{O_3 O_2} \rVert\,\lVert \overrightarrow{O_3 P} \rVert}
\right)
```

公式 (2.21) | PDF page 30
```latex
q_3 = -\pi + \arccos\left(
\frac{\lVert \overrightarrow{O_3 O_2} \rVert^2 + \lVert \overrightarrow{O_3 P} \rVert^2 - \lVert \overrightarrow{O_2 P} \rVert^2}{2\lVert \overrightarrow{O_3 O_2} \rVert\,\lVert \overrightarrow{O_3 P} \rVert}
\right)
```

公式 (2.22) | PDF page 31
```latex
\begin{cases}
x_p = (l_3 \cos q_3 + l_2)\sin q_2 + l_3 \sin q_3 \cos q_2, \\
y_p = -l_3 \sin q_1 \cos(q_2 + q_3) + l_1 \cos q_1 - l_2 \cos q_2 \sin q_1, \\
z_p = -l_3 \cos(q_2 + q_3) - l_2 \cos q_2.
\end{cases}
```

公式 (2.23) | PDF page 31
```latex
y_p \sin q_1 - z_p \cos q_1
= -l_3 \cos(q_2 + q_3)\left(\sin^2 q_1 + \cos^2 q_1\right) - l_2 \cos q_2\left(\sin^2 q_1 + \cos^2 q_1\right)
= l_3 \sin q_3 \sin q_2 - (l_3 \cos q_3 + l_2)\cos q_2
```

公式 (2.24) | PDF page 31
```latex
\frac{z_p}{y_p} = \frac{\sin q_1}{\cos q_1} = \tan q_1
```

公式 (2.25) | PDF page 31
```latex
L\left(y_p^2 + z_p^2\right) = 0
```

公式 (2.26) | PDF page 31
```latex
\frac{y_p \sin q_1 - z_p \cos q_1}{x_p}
=
\frac{l_3 \sin q_3 \sin q_2 - (l_3 \cos q_3 + l_2)\cos q_2}{(l_3 \cos q_3 + l_2)\sin q_2 + l_3 \sin q_3 \cos q_2}
```

公式 (2.27) | PDF page 32
```latex
\begin{cases}
a_1 = y_p \sin q_1 - z_p \cos q_1, \\
a_2 = x_p.
\end{cases}
```

公式 (2.28) | PDF page 32
```latex
\tan q_2 = \frac{a_1 m_1 + a_2 m_2}{a_2 m_1 - a_1 m_2}
```

公式 (2.29) | PDF page 32
```latex
q_2 = \operatorname{atan2}(a_1 m_1 + a_2 m_2,\, a_2 m_1 - a_1 m_2)
```

公式 (2.30) | PDF page 32
```latex
\begin{cases}
q_1 = \operatorname{atan2}(z_p l_1 + y_p L,\, y_p l_1 - z_p L), \\
q_2 = \operatorname{atan2}(a_1 m_1 + a_2 m_2,\, a_2 m_1 - a_1 m_2), \\
q_3 = -\pi + \arccos\left(\frac{l_2^2 + l_3^2 - \lVert \overrightarrow{O_2 P} \rVert^2}{2 l_2 l_3}\right).
\end{cases}
```

公式 (2.31) | PDF page 32
```latex
\begin{cases}
a_1 = y_p \sin q_1 - z_p \cos q_1, \\
a_2 = x_p, \\
m_1 = l_3 \sin q_3, \\
m_2 = l_2 + l_3 \cos q_3.
\end{cases}
```

公式 (2.32) | PDF page 33
```latex
m\ddot{p} = \sum_{i=1}^{n} f_i - mg
```

公式 (2.33) | PDF page 34
```latex
\frac{d}{dt}(I\omega) = \sum_{i=1}^{n} r_i \times f_i
```

公式 (2.34) | PDF page 34
```latex
\dot{R} = [\omega]_\times R
```

公式 (2.35) | PDF page 34
```latex
{}_W^B R = R_Z(\psi)R_Y(\theta)R_X(\phi)
```

公式 (2.36) | PDF page 34
```latex
\boldsymbol{\omega} =
\begin{bmatrix}
\cos\theta\cos\psi & -\sin\psi & 0 \\
\cos\theta\sin\psi & \cos\psi & 0 \\
-\sin\theta & 0 & 1
\end{bmatrix}
\begin{bmatrix}
\dot{\phi} \\
\dot{\theta} \\
\dot{\psi}
\end{bmatrix}
```

公式 (2.37) | PDF page 34
```latex
\begin{bmatrix}
\dot{\phi} \\
\dot{\theta} \\
\dot{\psi}
\end{bmatrix}
=
\begin{bmatrix}
\cos\psi/\cos\theta & \sin\psi/\cos\theta & 0 \\
-\sin\psi & \cos\psi & 0 \\
\sin\theta/\cos\theta & 0 & 1
\end{bmatrix}
\boldsymbol{\omega}
```

公式 (2.38) | PDF page 35
```latex
\begin{bmatrix}
\dot{\phi} \\
\dot{\theta} \\
\dot{\psi}
\end{bmatrix}
\approx
\begin{bmatrix}
\cos\psi & \sin\psi & 0 \\
-\sin\psi & \cos\psi & 0 \\
0 & 0 & 1
\end{bmatrix}
\boldsymbol{\omega}
= R_Z^{\mathrm{T}}(\psi)\boldsymbol{\omega}
```

公式 (2.39) | PDF page 35
```latex
\frac{d}{dt}(I\boldsymbol{\omega}) = I\dot{\boldsymbol{\omega}} + \boldsymbol{\omega} \times (I\boldsymbol{\omega})
```

公式 (2.40) | PDF page 35
```latex
I = R({}_B I)R^{\mathrm{T}}
```

公式 (2.41) | PDF page 35
```latex
\hat{I} = R_Z(\psi)({}_B I)R_Z^{\mathrm{T}}(\psi)
```

公式 (2.42) | PDF page 35
```latex
\dot{\boldsymbol{\omega}} = \hat{I}^{-1}\sum_{i=1}^{n} r_i \times f_i
```

公式 (2.43) | PDF page 35
```latex
\frac{d}{dt}
\begin{bmatrix}
\hat{\Theta} \\
\hat{p} \\
\hat{\omega} \\
\dot{\hat{p}} \\
\hat{g}
\end{bmatrix}
=
\mathbf{A}
\begin{bmatrix}
\hat{\Theta} \\
\hat{p} \\
\hat{\omega} \\
\dot{\hat{p}} \\
\hat{g}
\end{bmatrix}
+
\mathbf{B}
\begin{bmatrix}
f_1 \\
\vdots \\
f_n
\end{bmatrix}
```

公式 (2.44) | PDF page 35
```latex
\mathbf{A} =
\begin{bmatrix}
0_3 & 0_3 & R_Z^{\mathrm{T}}(\psi) & 0_3 & 0_3 \\
0_3 & 0_3 & 0_3 & I_3 & 0_3 \\
0_3 & 0_3 & 0_3 & 0_3 & 0_3 \\
0_3 & 0_3 & 0_3 & 0_3 & I_3 \\
0_3 & 0_3 & 0_3 & 0_3 & 0_3
\end{bmatrix}
```

公式 (2.45) | PDF page 35
```latex
\dot{x}(t) = A(\psi)x(t) + B(r_1,\ldots,r_n,\psi)u(t)
```

公式 (2.46) | PDF page 36
```latex
L = T - P
```

公式 (2.47) | PDF page 36
```latex
\tau_i = \frac{d}{dt}\left(\frac{\partial L}{\partial \dot{q}_i}\right) - \frac{\partial L}{\partial q_i}
```

公式 (2.48) | PDF page 37
```latex
I_1 = R_{0,abad}\,{}_{1}I\,R_{0,abad}^{\mathrm{T}},
\qquad
I_2 = R_{0,hip}\,{}_{2}I\,R_{0,hip}^{\mathrm{T}}
```

公式 (2.49) | PDF page 37
```latex
\begin{cases}
p_{1x} = 0, \\
p_{1y} = -a_1 l_1 \cos q_1.
\end{cases}
```

公式 (2.50) | PDF page 37
```latex
\begin{cases}
v_{1x} = 0, \\
v_{1y} = a_1 l_1 \dot{q}_1 \sin q_1.
\end{cases}
```

公式 (2.51) | PDF page 37
```latex
\boldsymbol{\omega}_1 =
\begin{bmatrix}
\dot{q}_1 \\
0 \\
0
\end{bmatrix}
```

公式 (2.52) | PDF page 37
```latex
\begin{cases}
p_{2x} = -a_2 l_2 \sin q_2, \\
p_{2y} = -l_1 \cos q_1 + a_2 l_2 \cos q_2 \sin q_1.
\end{cases}
```

公式 (2.53) | PDF page 37
```latex
\begin{cases}
v_{2x} = -a_2 l_2 \dot{q}_2 \cos q_2, \\
v_{2y} = \left(l_1 \sin q_1 + a_2 l_2 \cos q_1 \cos q_2\right)\dot{q}_1 - a_2 l_2 \dot{q}_2 \sin q_1 \sin q_2.
\end{cases}
```

公式 (2.54) | PDF page 37
```latex
\boldsymbol{\omega}_2 =
\begin{bmatrix}
\dot{q}_1 \\
\dot{q}_2 \cos q_1 \\
0
\end{bmatrix}
```

公式 (2.55) | PDF page 38
```latex
\begin{cases}
p_{3x} = -l_2 \sin q_2 - a_3 l_3 \sin(q_2 + q_3), \\
p_{3y} = -l_1 \cos q_1 + l_2 \cos q_2 \sin q_1 + a_3 l_3 \sin q_1 \cos(q_2 + q_3).
\end{cases}
```

公式 (2.56) | PDF page 38
```latex
\begin{aligned}
v_{3y} &= \left(l_1 \sin q_1 + l_2 \cos q_1 \cos q_2 + a_3 l_3 \cos q_1 \cos(q_2 + q_3)\right)\dot{q}_1 \\
&\quad + \left(l_2 \cos q_1 \sin q_2 + a_3 l_3 \cos q_1 \sin(q_2 + q_3)\right)\dot{q}_2 \\
&\quad + a_3 l_3 \dot{q}_3 \cos q_1 \sin(q_2 + q_3)
\end{aligned}
```

公式 (2.57) | PDF page 38
```latex
\boldsymbol{\omega}_3 =
\begin{bmatrix}
\dot{q}_1 \\
(\dot{q}_2 + \dot{q}_3)\cos q_1 \\
0
\end{bmatrix}
```

公式 (2.58) | PDF page 38
```latex
T_{\mathrm{trans}} = \frac{1}{2}m_1 v_1^2 + \frac{1}{2}m_2 v_2^2 + \frac{1}{2}m_3 v_3^2
```

公式 (2.59) | PDF page 38
```latex
T_{\mathrm{rot}} = \frac{1}{2}\boldsymbol{\omega}_1^{\mathrm{T}}{}_{0}I_1\boldsymbol{\omega}_1 + \frac{1}{2}\boldsymbol{\omega}_2^{\mathrm{T}}{}_{0}I_2\boldsymbol{\omega}_2 + \frac{1}{2}\boldsymbol{\omega}_3^{\mathrm{T}}{}_{0}I_3\boldsymbol{\omega}_3
```

公式 (2.60) | PDF page 38
```latex
T = T_{\mathrm{trans}} + T_{\mathrm{rot}}
```

公式 (2.61) | PDF page 38
```latex
P = P_1 + P_2 + P_3 = m_1 g p_{1z} + m_2 g p_{2z} + m_3 g p_{3z}
```

公式 (2.62) | PDF page 39
```latex
M(q,t)\ddot{q} + C(q,\dot{q},t)\dot{q} + G(q,t) = \tau(t)
```

公式 (2.63) | PDF page 39
```latex
\begin{aligned}
M_{11} &= \frac{1}{2}\left(I_{xx2}\cos 2q_2 - I_{zz2}\cos 2q_2 + I_{xx3}\cos(2q_2 + 2q_3) - I_{zz3}\cos(2q_2 + 2q_3)\right) \\
&\quad + m_1 a_1^2 l_1^2 + m_2 l_1^2 + m_2 a_2^2 l_2^2 + \frac{1}{2}m_2 a_2^2 l_2^2\cos 2q_2 \\
&\quad + m_3 l_1^2 + \frac{1}{2}m_3 l_2^2 + \frac{1}{2}m_3 l_2^2\cos 2q_2 + m_3 l_2 l_3 a_3 \cos q_3 \\
&\quad + \frac{1}{2}m_3 a_3^2 l_3^2 + \frac{1}{2}m_3 a_3^2 l_3^2 \cos(2q_2 + 2q_3) + m_3 l_2 l_3 a_3 \cos(2q_2 + q_3)
\end{aligned}
```

公式 (2.64) | PDF page 39
```latex
M_{12} = -m_2 l_1 l_2 a_2 \sin q_2 - m_3 l_1 l_2 \sin q_2 - m_3 l_1 l_3 a_3 \sin(q_2 + q_3)
```

公式 (2.65) | PDF page 39
```latex
M_{13} = -m_3 l_1 l_3 a_3 \sin(q_2 + q_3)
```

公式 (2.66) | PDF page 39
```latex
M_{21} = -m_2 l_1 l_2 a_2 \sin q_2 - m_3 l_1 l_2 \sin q_2 - m_3 l_1 l_3 a_3 \sin(q_2 + q_3)
```

公式 (2.67) | PDF page 39
```latex
M_{22} = m_2 a_2^2 l_2^2 + m_3 l_2^2 + 2m_3 l_2 l_3 a_3 \cos q_3 + m_3 a_3^2 l_3^2 + I_{yy2} + I_{yy3}
```

公式 (2.68) | PDF page 39
```latex
M_{23} = m_3 a_3^2 l_3^2 + m_3 l_2 l_3 a_3 \cos q_3 + I_{yy3}
```

公式 (2.69) | PDF page 39
```latex
M_{31} = -m_3 l_1 l_3 a_3 \sin(q_2 + q_3)
```

公式 (2.70) | PDF page 39
```latex
M_{32} = m_3 a_3^2 l_3^2 + m_3 l_2 l_3 a_3 \cos q_3 + I_{yy3}
```

公式 (2.71) | PDF page 39
```latex
M_{33} = m_3 a_3^2 l_3^2 + I_{yy3}
```

公式 (2.72) | PDF page 39
```latex
\begin{aligned}
C_{11} &= -\dot{q}_2\Big(m_2 a_2^2 l_2^2 \sin 2q_2 + m_3 l_2^2 \sin 2q_2 + 2m_3 l_2 l_3 a_3 \sin(2q_2 + q_3) \\
&\qquad + m_3 a_3^2 l_3^2 \sin(2q_2 + 2q_3) + I_{xx3} \sin(2q_2 + 2q_3) - I_{zz3} \sin(2q_2 + 2q_3) \\
&\qquad + I_{xx2} \sin 2q_2 - I_{zz2} \sin 2q_2\Big) \\
&\quad - \dot{q}_3\Big(I_{xx3} \sin(2q_2 + 2q_3) - I_{zz3} \sin(2q_2 + 2q_3) + m_3 a_3^2 l_3^2 \sin(2q_2 + 2q_3) \\
&\qquad + m_3 l_2 l_3 a_3 \sin q_3 + m_3 l_2 l_3 a_3 \sin(2q_2 + q_3)\Big)
\end{aligned}
```

公式 (2.73) | PDF page 39
```latex
C_{12} = -\dot{q}_2\left(m_3 l_1 l_3 \cos q_2 + m_3 l_1 l_3 a_3 \cos(q_2 + q_3) + m_2 l_1 l_2 a_2 \cos q_2\right) - 2\dot{q}_3 l_1 l_3 a_3 \cos(q_2 + q_3)
```

公式 (2.74) | PDF page 39
```latex
C_{13} = -\dot{q}_3\left(m_3 l_1 l_3 a_3 \cos(q_2 + q_3)\right)
```

公式 (2.75) | PDF page 40
```latex
C_{21} = \text{OCR 残缺，该式在原 PDF 中位于 } C_{13} \text{ 与 } C_{22} \text{ 之间，建议对照原文补全。}
```

公式 (2.76) | PDF page 40
```latex
C_{22} = -2\dot{q}_3 m_3 l_2 l_3 a_3 \sin q_3
```

公式 (2.77) | PDF page 40
```latex
C_{31} = \dot{q}_1\left(I_{xx3} \sin(2q_2 + 2q_3) - I_{zz3} \sin(2q_2 + 2q_3) + m_3 a_3^2 l_3^2 \sin(2q_2 + 2q_3) + m_3 l_2 l_3 a_3 \sin q_3 + m_3 l_2 l_3 a_3 \sin(2q_2 + q_3)\right)
```

公式 (2.78) | PDF page 40
```latex
C_{32} = \dot{q}_2 m_3 l_2 l_3 a_3 \sin q_3
```

公式 (2.79) | PDF page 40
```latex
C_{33} = 0
```

公式 (2.80) | PDF page 40
```latex
G_1 = -m_1 g l_1 a_1 \cos q_1 - m_2 g\left(l_1 \cos q_1 - l_2 a_2 \sin q_1 \cos q_2\right) - m_3 g\left(l_1 \cos q_1 - l_2 \sin q_1 \cos q_2 - l_3 a_3 \sin q_1 \cos(q_2 + q_3)\right)
```

公式 (2.81) | PDF page 40
```latex
G_2 = m_2 g l_2 a_2 \sin q_2 \cos q_1 + m_3 g l_2 \sin q_2 \cos q_1 + m_3 g l_3 a_3 \sin(q_2 + q_3) \cos q_1
```

公式 (2.82) | PDF page 40
```latex
G_3 = m_3 g l_3 a_3 \sin(q_2 + q_3) \cos q_1
```

公式 (3.1) | PDF page 44
```latex
x_f = x_b + v_x T_{swing} + \Delta x
```

公式 (3.2) | PDF page 44
```latex
x_f = x_b + v_x T_{swing} + \frac{1}{2}v_x T_{stance} + k_x\left(v_x - v_{xd}\right)
```

公式 (3.3) | PDF page 45
```latex
\psi_f = \psi_0 + \psi + \omega T_{swing} + \omega T_{stance} + k_{\omega}(\omega - \omega_d)
```

公式 (3.4) | PDF page 45
```latex
\begin{cases}
x_f = R\cos \psi_f, \\
y_f = R\sin \psi_f.
\end{cases}
```

公式 (3.5) | PDF page 45
```latex
x_f = x_b + v_x T_{swing} + \frac{1}{2}v_x T_{stance} + k_x\left(v_x - v_{xd}\right) + R\cos \psi_f
```

公式 (3.6) | PDF page 45
```latex
B(t) = \sum_{i=0}^{n} \binom{n}{i} P_i (1-t)^{n-i} t^i
```

公式 (3.7) | PDF page 48
```latex
(p - p_0)^{\mathrm{T}} n = 0
\iff
z = \frac{d - ax - by}{c},
\qquad
d = ax_0 + by_0 + cz_0
```

公式 (3.8) | PDF page 48
```latex
\begin{bmatrix}
z_1 \\
z_2 \\
\vdots \\
z_n
\end{bmatrix}
=
\begin{bmatrix}
-x_1 & -y_1 & 1 \\
-x_2 & -y_2 & 1 \\
\vdots & \vdots & \vdots \\
-x_n & -y_n & 1
\end{bmatrix}
\begin{bmatrix}
a \\
b \\
c
\end{bmatrix}
\Rightarrow z = W\pi
```

公式 (3.9) | PDF page 48
```latex
W^{\mathrm{T}} z = W^{\mathrm{T}} W\pi
```

公式 (3.10) | PDF page 49
```latex
\phi_{roll} = \arctan\left(\frac{b}{c}\right)
```

公式 (3.11) | PDF page 50
```latex
\Delta x = -\tan \theta \cdot h
```

公式 (3.12) | PDF page 50
```latex
x_f = x_b + v_x T_{swing} + v_x T_{stance} + k_x\left(v_x - v_{xd}\right) + R\cos \psi_f + \Delta x
```

公式 (3.13) | PDF page 50
```latex
\Delta y = -\tan \phi \cdot h
```

公式 (3.14) | PDF page 50
```latex
y_f = y_b + v_y T_{swing} + v_y T_{stance} + k_y\left(v_y - v_{yd}\right) + R\sin \psi_f + \Delta y
```
