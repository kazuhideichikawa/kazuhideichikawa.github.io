# 「入門 情報幾何」第2章(フィッシャー計量)

第１章では、
- 統計的モデル(p.14、パラメターで表される確率関数の族)
- 十分統計量(p.26、統計的モデルの事象に対する写像)

が導入された。

1. TOC
{:toc}

## 2.1 リーマン計量

p.36の１行目で、「標準内積と限らない内積」が出てくるが、これの定義・説明が出てこないような気がする。(p.40で使っている内積の線形性・対称性・正値性の説明は？)

p.39、式(2.24)の計算で使う式：
$$ (\log \tan x)^\prime = \frac{1}{\sin x \cos x}= \frac{2}{\sin 2x}$$
$$ \tan \frac{\pi-\theta}{2} = \left( \tan\frac{\theta}{2} \right)^{-1}$$

式(2.25)は、(2.22)(2.24)より、
$$ f(\theta) = 2 (L(\gamma_3)-L(\gamma_4)) $$
を計算している。

## 2.2 写像の微分

p.44 
十分統計量は、第1章で定義されたように写像なので、微分を考えることができ、それが「はめ込み(immersion)」（単射）かどうかを考えることができる。例2.3,2.4,2.5にて、それぞれ例1.17,1.18,1.19で定義した十分統計量がはめ込みであることが示されている。

p.44　例2.3

$n=3$で具体的に考えてみる。$F_3$は、$$
F_3=
\begin{pmatrix}
1 & 2 & 3 \\
3 & 1 & 2 \\
\end{pmatrix}$$という置換で考える。すると、逆変換は
$$F_3^{-1}=
\begin{pmatrix}
1 & 2 & 3 \\
2 & 3 & 1 \\
\end{pmatrix}$$
である。よって、式(2.47)の写像は、
$$ \Phi_3(\xi_1, \xi_2, \xi_3) = (\xi_2, \xi_3, \xi_1) $$である(添字を $F_3^{-1}$ で置換したもの)。
$\Phi_3$ の第$j$成分を$\Phi_3^{(j)}$とすると、
$$ \Phi_3^{(1)}=\xi_2,\quad \Phi_3^{(2)}=\xi_3,\quad \Phi_3^{(3)}=\xi_1 $$となるので、(2.40)を具体的に書くと(i,jの順番に注意。iは縦に、jは横に増える。)、
$$
J_{\Phi_3(\xi)} = \left( \frac{\partial \Phi_3^{(j)}}{\partial \xi_i} \right)= 
\begin{pmatrix}
\frac{\partial \Phi_3^{(1)}}{\partial \xi_1} & \frac{\partial \Phi_3^{(2)}}{\partial \xi_1} & \frac{\partial \Phi_3^{(3)}}{\partial \xi_1} \\
\frac{\partial \Phi_3^{(1)}}{\partial \xi_2} & \frac{\partial \Phi_3^{(2)}}{\partial \xi_2} & \frac{\partial \Phi_3^{(3)}}{\partial \xi_2} \\
\frac{\partial \Phi_3^{(1)}}{\partial \xi_3} & \frac{\partial \Phi_3^{(2)}}{\partial \xi_3} & \frac{\partial \Phi_3^{(3)}}{\partial \xi_3} \\
\end{pmatrix}=
\begin{pmatrix}
0 & 0 & 1 \\
1 & 0 & 0 \\
0 & 1 & 0 \\
\end{pmatrix}=
\begin{pmatrix}
e_3 \\
e_1 \\
e_2 \\
\end{pmatrix}=
\begin{pmatrix}
e_{F_3(1)} \\
e_{F_3(2)} \\
e_{F_3(3)} \\
\end{pmatrix}
$$
で、(2.48)の形になっている($e_i$は、第$i$成分だけが1の横ベクトル)

$n$個の置換で一般的に考えると、$\left( \frac{\partial \Phi_n^{(j)}}{\partial \xi_i} \right) $がゼロにならないのは、
$\Phi_n^{(j)} = \xi_i$となる$j$の時。これがどの$j$かを考えると、$\Phi_n^{(j)}$は(2.47)の定義より、 $$\xi_{F^{-1}_n(j)}$$ なので、これは $$\xi_i = \xi_{F^{-1}_n(j)}$$ 、つまり $i =F^{-1}_n(j)$ 、よって $j=F_n(i)$ の時。
別の言い方をすると、 $i$ 行目の単位横ベクトルは、第 $F_n(i)$ 成分だけ1ということで、(2.48)を意味する。