---
numbersections: false
---

# [TK: section heading]


Ist $(a_1,...,a_m)$ eine Familie von Vektoren aus $K^n,$ so ist $U=span(a_1,...,a_m)$ der erzeugte Untervektorraum. Aus dem Basisauswahlsatz folgt: Basis = "unverkürzbares" Erzeugendensystem (kann sehr aufwendig sein)

Betrachte $a_1 = \begin{pmatrix} a_{11} \\ \vdots \\ a_{1n} \end{pmatrix},..., a_m = \begin{pmatrix} a_{m1} \\ \vdots \\ a_{mn} \end{pmatrix} \in K^n.$

Bilde die folgende Matrix $A = \begin{pmatrix} a_{11} & ... & a_{m1} \\
\vdots & & vdots \\ a_{1n} & ... & a_{mn} \end{pmatrix} = \begin{pmatrix} a_1^T \\ \vdots \\ a_m^T \end{pmatrix}$


## Definiton 4.1

Der von den Zeilenvektoren $A_{i \bullet} \in K^n$ von A aufgespannte Untervektorraum von $K^n$ heißt der $\textbf{Zeilenraum}$ von A und wird mit ZR(A) bezeichnet: $ZR(A) = span(A_{1 \bullet},...,A_{m \bullet}) \subseteq K^n$. Entsprechend heißt der von den Spaltenvektoren $A_{\bullet j} \in K^m$ aufgespannte Untervektorraum von $K^m$ der $\textbf{Spaltenraum}$ von A und wird mit SR(A) bezeichnet: $SR(A) = span(A_{\bullet 1},...,A_{\bullet n}) \subseteq K^m$.
Die Dimension von ZR(A) heißt der $\textbf{Zeilenrang}$ von A und die Dimension von SR(A) heißt der $\textbf{Spaltenrang}$ von A.


## Bemerkung

Beachte: A ~ (m,n) $\Rightarrow ZR(A) \subseteq K^n$ und $SR(A) \subseteq K^m$ und in der Regel $n \neq m$.

Später: Zeilenrang = Spaltenrang


## Beispiel

$A = \begin{pmatrix} 1 & 0 & 3 \\ 2 & -1 & 1 \end{pmatrix}$

$ZR(A) = span(\begin{pmatrix} 1 \\ 0 \\ 3 \end{pmatrix}, \begin{pmatrix} 2 \\ -1 \\ 1 \end{pmatrix}) \subseteq \mathbb{R}^3 \Rightarrow$ Zeilenrang = 2

$SR(A) = span(\begin{pmatrix} 1 \\ 2 \end{pmatrix}, \begin{pmatrix} 0 \\ -1 \end{pmatrix}, \begin{pmatrix} 3 \\ 1 \end{pmatrix}) \subseteq \mathbb{R}^3
\Rightarrow$ Spaltenrang = 2


## Definition 4.2

Eine Matrix $B = (b_{ij})$ ~ (m,n) heißt eine $\textbf{Matrix in Zeilenstufenform}$, wenn sie folgendes Aussehen hat:

\begin{tikzpicture}
    \node at (-3,0) {B =};
    \matrix (m) at (0.5,0) [ matrix of nodes, row sep = 0.1em, column sep = 0em,
                 nodes={minimum width = 3em, outer sep = 0em},
                 left delimiter={(}, right delimiter={)}] {
            $\ast$      &           &           &           &             \\
                        & $\ast$    &           &           &             \\
                        &           & $\ast$    &           &             \\
                        &           &           & \cdots    & $b_r$       \\
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

Dabei müssen die Einträge an den mit * markierten Stellen ungleich 0 sein und unterhalb der "Stufenlinie" müssen alle Einträge 0 sein. Genauer:

(1) Es gibt eine Zahl r, $0 \leq r \leq m$, sodass in den Zeilen 1 bis r jeweils mindestens ein von 0 verschiedener Eintrag steht und in den Zeilen r+1 bis n alle Einträge 0 sind.

(2) Für jedes i mit $1 \leq i \leq r$ bezeichne $j_i$ die niedrigste Nummer der Spalten, in denen ein Eintrag ungleich 0 steht, also $j_i = min \{j | b_{ij} \neq 0 \}$. Natürlich ist $1 \leq j_i \leq n.$ Dann lautet die Stufenbedingung: $j_1 < ... < j_r.$


## Bemerkung

Für r = 0 ist natürlich B = 0. Die oben durch * markierten Einträge sind genau die Elemente $b_{1 j_1},...,b_{r j_r}$. Sie heißen **Pivots** (Angelpunkte) bzw. Pivotelemente von B.


## Beispiel

### Leo ergänzt hier ein Diagramm

$m = 4, n = 7, r = 3, j_1 = 2, j_2 = 3, j_3 = 6, b_{1 j_1} = 6, b_{2 j_2}, b_{3 j_3} = 5$


## Folgerung

Sei $B = (b_{ij})$ eine Matrix in Zeilenstufenform. Dann bilden die ersten r Zeilenvektoren $B_{1 \bullet},...,B_{r \bullet}$ von B eine Basis des Zeilenraums ZR(B) und es gilt dim(ZR(B)) = r.

Beweis:

$\alpha_1 \cdot B_{1 \bullet} + ... + \alpha_r \cdot B_{r \bullet} = 0 \Rightarrow \alpha_1 \cdot b_{1 j_1} = 0 \Rightarrow \alpha_1 = 0,$ da $b_{1 j_1} \neq 0$. Also folgt: $\alpha_2 \cdot B_{2 \bullet} + ... + \alpha_r \cdot B_{r \bullet} = 0 \Rightarrow \alpha_2 \cdot b_{2 j_2} = 0 \Rightarrow \alpha_2  = 0$, da $b_{2 j_2} \neq 0.$
Usw. bis letztendlich folgt $\alpha_r = 0.$


## Definition 4.3

Folgende Operationen bezeichnet man als **elementare Zeilenumformungen** einer Matrix:

(I) Multiplikation einer i-ten Zeile von A mit einem Skalar $\alpha \in K, \alpha \neq 0.$


(II) Addition der j-ten Zeile von A zur i-ten Zeile von A, wobei $i \neq j.$


(III) Addition der $\alpha$-fachen j-ten Zeile zur i-ten Zeile von A, wobei $i \neq j.$


(IV) Vertauschen der i-ten Zeile mit der j-ten Zeile, wobei $i \neq j.$




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
