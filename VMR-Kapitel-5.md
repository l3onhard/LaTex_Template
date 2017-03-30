---
header-includes:
- \usepackage[all]{xy}
- \usepackage{tikz}
- \usetikzlibrary{calc,matrix}
---

# 5. Lineare Gleichungssysteme

Nach [Lemma 1.8] und [Lemma 4.4] definiert jede Matrix $A: K^n \to K^m$ durch $x \mapsto Ax$.

## Defininition 5.1

Ist $A = (a_{ij}) \sim (m, n)$ eine Matrix und $b = \begin{pmatrix} b_{1} \\ \vdots \\ b_{m} \end{pmatrix} \in K^m$, so heißt:

$$
Ax = b \iff
\begin{matrix}
a_{11} x_{1} + \cdots + a_{1n} x_{n} = b_{1} \\
\vdots \\
a_{m1} x_{1} + \cdots + a_{mn} x_{n} = b_{m}
\end{matrix}
$$

ein **lineares Gleichungssystem** mit $m$ Gleichungen und $n$ Unbekannten.

Ist $b \neq 0$, so heißt das lineare Gleichungssystem **inhomogen**, andernfalls **homogen**. $Ax = 0$ heißt, dass zu dem inhomogenen System gehörende homogene lineare Gleichungssystem.

Die Menge $\mathbb{L}(A,b) = \{x \in K^n | Ax = b\} \subset K^n$ heißt der Lösungsraum des linearen Gleichungssystems $Ax = b$ ($b = 0$ oder $b \neq 0$).

$A$ heißt die **Koeffizientenmatrix**, die Einträge $a_{ij}$ **Koeffizienten** des linearen Gleichungssystems. Die Matrix $(A|b)$ heißt die **erweiterte Matrix des linearen Gleichungssystems** $Ax = b$.

### Bemerkung

Bezeichnet $f: K^n \to K^m$ mit $f(x) = Ax$ die durch $A \sim (m,n)$ definiertes lineare Abbildung, so gilt:

$$ \begin{aligned}
\mathbb{L}(A, b) &= f^{-1}(b)\ \text{(Menge der Urbilder von b unter f)} \\
\mathbb{L}(A, 0) &= Ker f
\end{aligned} $$

### Beispiel

$$ \begin{aligned}
&\begin{matrix}
2 x_1 - 3 x_2 + x_3 &= 5 \\
- x_1 + 2 x_2 + 4 x_3 &= 1 \\
x_1 - x_2 &= 2
\end{matrix}
\ \ \ \hat{=} \ \
\begin{pmatrix}
2  & -3 & 1 & \BAR & 5 \\
-1 & 2  & 4 & \BAR & 1 \\
1  & -1 & 0 & \BAR & 2
\end{pmatrix} \text{erweiterte Matrix}\  (A|b) \\[3mm]
&\begin{pmatrix}
2  & -3 & 1 \\
-1 & 2  & 4 \\
1  & -1 & 0
\end{pmatrix}
\begin{pmatrix}
x_1 \\
x_2 \\
x_3
\end{pmatrix}
=
\begin{pmatrix}
5 \\
1 \\
2
\end{pmatrix} \\
&\text{Koeffizientenmatrix}
\end{aligned} $$

## Satz 5.2

Gegeben sei das LGS $A \cdot x=b$, wobei $A \sim (m,n)$. Sei $r$ der Spaltenrang von $A$, d.h. $r = dim(SR(A))$. Dann gilt:

1) $\mathbb{L}(A,0) \subseteq K^n$ ist $(n-r)$-dimensionaler UVR
2) $\mathbb{L} = \emptyset$ oder $\mathbb{L}(A,b)$ hat folgende Form:
$$\mathbb{L}(A,b) = v + \mathbb{L}(A,0) \text{ , wobei } v \in \mathbb{L}(A,b) \text{ eine beliebige Lösung ist}$$

### Beweis

(1) Sei $f: K^n \to K^m$ die durch A definierte lineare Abbildung mit $f(x) = A \cdot x$. Die Spalten von $A$ sind genau die Bilder $f(e_j)$ der Standardbasisvektoren: $f(e_j) = A \cdot e_j = A_{\cdot j}$. \newline Daher sind die Spaltenvektoren von $A$ ein EZS von $Im(f)$, d.h. es gilt $Im(f) = SR(A)$. Daraus folgt $dim(Im(f)) = r$. \newline Mit der Dimensionsformel (siehe 6.2) folgt:
$$ dim(K^n) = dim(Ker(f)) + dim(Im(f)) \iff n = dim(Ker(f)) + r $$ \newline Daraus folgt: $dim(Ker(f)) = n - r$. \newline Da $Ker(f) = \mathbb{L}(A,0) \subseteq K^n$ ist UVR mit $dim(\mathbb{L}(A,0)) = n-r$.

(2) Sei $w \in \mathbb{L}(A,0)$ und $v \in \mathbb{L}(A,b)$, d.h. $A \cdot w = 0$ und $A \cdot v = b$. \newline
$\implies A \cdot (v+w) = A \cdot v + A \cdot w = b + 0 = b \quad\implies v + w \in \mathbb{L}(A,b)$ \newline
$\implies v + \mathbb{L}(A,0) \subseteq \mathbb{L}(A,b)$ \newline
Sei $v' \in \mathbb{L}(A,b)$ eine weitere Lösung, d.h. $A \cdot v' = b$. \newline
$\implies A \cdot (v-v') = A \cdot v - A \cdot v' = b - b = 0 \quad\implies v - v' \in \mathbb{L}(A,0)$ \newline
$\implies v' \in v + \mathbb{L}(A,0) \quad\implies \mathbb{L}(A,b) \subseteq v + \mathbb{L}(A,0)$

### Bemerkung
- $\mathbb{L}(A,0) \neq \emptyset$, da $0 \in \mathbb{L}(A,0)$
- $0$ heißt die triviale Lösung des homogenen Systems.
- Ein inhomogenes System hat nicht immer Lösungen.

## Satz 5.3

Für ein inhomogenes LGS $A \cdot x = b$ mit $A \sim (m,n)$ gilt:
$$\mathbb{L}(A,b) \neq \emptyset \iff \text{Spaltenrang}(A) = \text{Spaltenrang}((A|b))$$

### Beweis
Definiere: Spaltenrang$(A)$ $=$ Rg$(A)$, Spaltenrang$((A|b))$ $=$ Rg$((A|b))$ \newline
Mit Rg$(A)$ $=$ $r$ gilt: $r \leq Rg((A|b)) \leq r + 1$. \newline
$$ \begin{aligned} \mathbb{L}(A,b) \neq \emptyset &\iff \exists v \in K^n \ \text{mit} \ A \cdot v = b \\
& \iff v_1 \cdot A_{\bullet 1} + \dots + v_n \cdot A_{\bullet n} = b \\
& \iff b \text{ ist Linearkombination der Spalten von } A \\
& \iff b \text{ ist Linearkombination der } r \text{ linear unabhängigen Spalten von } A \\
& \iff Rg((A|b)) = r
\end{aligned} $$

## Lemma 5.4
Sei $A \cdot x = b$ ein LGS und die Koeffizientenmatrix $A$ in Zeilenstufenform, Pivots in den ersten $r$ Spalten sitzen, $a_{11} \neq 0, \ldots , a_{rr} \neq 0, r \leq m$ und $r \leq n$:




\begin{tikzpicture}
   \matrix (m) [ matrix of nodes, row sep = 0.1em, column sep = 0em,
                 nodes={minimum width = 3em, outer sep = 0em},
                 left delimiter={(}, right delimiter={)}] {
            $a_{11}$    &           &           &           & $b_1$       \\
                        & $a_{22}$  &           &           & $b_2$       \\
                        &           & $\ddots$  &           & $\vdots$    \\
                        &           &           & $a_{rr}$  & $b_r$       \\
                        &           &           &           & $b_{r+1}$   \\
                        &           &           &           & $\vdots$    \\
                        &           &           &           & $b_m$       \\
   };
    \draw  (m-1-1.south west) -- (m-1-1.south east)
        -- (m-2-2.south west) -- (m-2-2.south east)
        -- (m-3-3.south west) -- (m-3-3.south east)
        -- (m-4-4.south west) -- (m-4-4.south east)
        -- (m-4-5.south west) -- (m-4-5.south east);
    \draw  (m-1-5.north west) -- (m-7-5.south west);
   \node[anchor=south west] at ([shift={(10mm,10mm)}]m.south west) {\Huge 0};
\end{tikzpicture}
