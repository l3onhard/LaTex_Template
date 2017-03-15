---
numbersections: false
---

# [TK: section heading]

## Bemerkung

Die elementaren Umformungen (III) und (IV) kann man durch Kombination der Umformungen (I) und (II) erhalten

## Lemma 4.4

Entsteht die Matrix $B$ aus der Matrix $A$ durch elementare Zeilenumformungen, so ist:

$$
ZR(B) = ZR(A)
$$

### Beweis

Nach der Bemerkung reicht es die Umformungen (I) und (II) zu betrachten:

$$
A = \begin{pmatrix}
a_{1}^T\\
\vdots \\
a_{m}^T
\end{pmatrix}
$$

#### 1) Sei $B = A_{I}$:

$$ \begin{aligned}
v &\in ZR(A) = span(a_{1}, \cdots, a_{m}) \\[3mm]
\implies v &= \alpha_{1} a_{1} + \cdots + \alpha_{i} a_{i} + \cdots + \alpha_{m} a_{m} \\
&= \alpha_{1} a_{1} + \cdots + \frac{\alpha_{i}}{\alpha} \alpha a_{i} + \cdots + \alpha_{m} a_{m} \in ZR(B)
\end{aligned} $$

Entsprechend folgt für $v \in ZR(B) = span(a_{1}, \cdots , \alpha a_{i}, \cdots , a_{m})$:

$$ \begin{aligned}
v &= \alpha_{1} a_{1} + \cdots + \alpha_{i} (\alpha a_{i}) + \cdots + \alpha_{m} a_{m} \\
&= \alpha_{1} a_{1} + \cdots + (\alpha_{i} \alpha) a_{i} + \cdots + \alpha_{m} a_{m} \in ZR(A)
\end{aligned} $$

Also ist $ZR(B) = ZR(A)$ .

#### 2) Sei $B = A_{II}$:

$$ \begin{aligned}
v &\in ZR(A) = span(a_{1}, \cdots, a_{m}) \\[3mm]
\implies v &= \alpha_{1} a_{1} + \cdots + \alpha_{i} a_{i} + \cdots + \alpha_{j} a_{j} + \cdots + \alpha_{m} a_{m} \\
&= \alpha_{1} a_{1} + \cdots + \alpha_{i} (a_{i} + a_{j}) + \cdots + (\alpha_{j} - \alpha_{i}) a_{j} + \cdots + \alpha_{m} a_{m} \in ZR(B)
\end{aligned} $$

und

$$ \begin{aligned}
v &\in ZR(B) \in span(a_{1}, \cdots, a_{i} + a_{j},\cdots, a_{j}, \cdots, a_{m}) \\[3mm]
\implies v &= \alpha_{1} a_{1} + \cdots + \alpha_{i} (a_{i} + a_{j}) + \cdots + \alpha_{j} a_{j} + \cdots + \alpha_{m} a_{m} \\
&= \alpha_{1} a_{1} + \cdots + \alpha_{i} a_{i} + \cdots + (\alpha_{j} + \alpha_{i}) a_{j} + \cdots + \alpha_{m} a_{m}
 \in ZR(A)
\end{aligned} $$

Also ist $ZR(A) = ZR(B)$.

## Satz 4.5

Jede Matrix $A$ kann durch elementare Zeilenumformungen in eine Matrix $\tilde{A}$ in Zeilenstufenform überführt werden.

### Beispiel

$$ \begin{aligned}
a_{1} &= \begin{pmatrix}
0 \\
0 \\
0 \\
2 \\
1
\end{pmatrix},
a_{2} = \begin{pmatrix}
0 \\
1 \\
2 \\
2 \\
0
\end{pmatrix},
a_{3} = \begin{pmatrix}
0 \\
-1 \\
2 \\
1 \\
-1
\end{pmatrix},
a_{4} = \begin{pmatrix}
0 \\
0 \\
0 \\
1 \\
2
\end{pmatrix} \\[3mm]
U &= span(a_{1}, a_{2}, a_{3}, a_{4})
\end{aligned} $$

\begin{align*}
A &= \begin{gmatrix}[p]
0 & 0 & 0 & 2 & -1 \\
0 & 1 & -2 & 1 & 0 \\
0 & -1 & 2 & 1 & -1 \\
0 & 0 & 0 & 1 & 2
\rowops
	\swap{0}{1}
\end{gmatrix}
\to
\begin{gmatrix}[p]
0 & 1 & -2 & 1 & 0 \\
0 & 0 & 0 & 2 & -1 \\
0 & -1 & 2 & 1 & -1 \\
0 & 0 & 0 & 1 & 2
\rowops
	\add[1]{0}{3}
\end{gmatrix} \\[3mm]
&\to
\begin{gmatrix}[p]
0 & 1 & -2 & 1 & 0 \\
0 & 0 & 0 & 2 & -1 \\
0 & 0 & 0 & 2 & -1 \\
0 & 0 & 0 & 1 & 2
\rowops
	\swap{1}{3}
\end{gmatrix}
\to
\begin{gmatrix}[p]
0 & 1 & -2 & 1 & 0 \\
0 & 0 & 0 & 1 & 2 \\
0 & 0 & 0 & 2 & -1 \\
0 & 0 & 0 & 2 & -1
\rowops
	\add[-2]{1}{2}
	\add[-2]{1}{3}
\end{gmatrix} \\[3mm]
&\to
\begin{gmatrix}[p]
0 & 1 & -2 & 1 & 0 \\
0 & 0 & 0 & 1 & 2 \\
0 & 0 & 0 & 0 & -5 \\
0 & 0 & 0 & 0 & -5
\rowops
	\add[-1]{2}{3}
\end{gmatrix}
\to
\begin{gmatrix}[p]
0 & 1 & -2 & 1 & 0 \\
0 & 0 & 0 & 1 & 2 \\
0 & 0 & 0 & 0 & -5 \\
0 & 0 & 0 & 0 & 0
\end{gmatrix}
= B
\end{align*}

Also ist $(b_{1}, b_{2}, b_{3})$ mit:

$$ \begin{aligned}
b_{1} &= \begin{pmatrix}
0 \\
1 \\
2 \\
1 \\
0
\end{pmatrix},
b_{2} = \begin{pmatrix}
0 \\
0 \\
0 \\
1 \\
2
\end{pmatrix},
b_{3} = \begin{pmatrix}
0 \\
0 \\
0 \\
0 \\
5
\end{pmatrix}
\end{aligned} $$

eine Basis von $U = span(a_{1}, a_{2}, a_{3}, a_{4})$.

## Korollar 4.6

Für Vektoren $v_{1}, \cdots, v_{n} \in K^n$ sind folgende Aussagen äquivalent:

1) $(v_{1}, \cdots, v_{n})$ ist Basis von $K^n$.
2) Die Matrix $A = \begin{pmatrix} v_{1}^T \\ \vdots \\ v_{n}^T \end{pmatrix}$ lässt sich durch elemntare Zeilenumformungen in eine obere Dreiecksmatrix überführen und alle Einträge auf der Hauptdiagonalen sind $\neq 0$.