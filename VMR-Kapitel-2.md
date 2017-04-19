# Kapitel 2: Matrizen, Rechnen mit Matrizen, spezielle Matrizen

## Definition 2.1

Sei A $\in K^{m\times n}$ eine Matrix. Die Matrix, deren Spalten die Zeilen von A sind, heißt die $\textbf{Transponierte von A}$ und wird mit $A^{T}$ (oft auch $A^{'}$ oder $A^{t}$) bezeichnet. Sie ist vom Typ $n\times m$:

$$
A = 
\begin{pmatrix}
a_{11}   & \dots & a_{1n} \\
\vdots &       & \vdots \\
a_{m1}   & \dots & a_{mn} \\
\end{pmatrix}
\in K^{m\times n} \Rightarrow A^{T} =
\begin{pmatrix}
a_{11}   & \dots & a_{m1} \\
\vdots &       & \vdots \\
a_{1n}   & \dots & a_{mn} \\
\end{pmatrix}
\in K^{n\times m}
$$

$$
A = (a_{ij}) \Rightarrow A^{T} = (a_{ji})
$$


## Beispiele


$$ (1) \text{ } A =
\begin{pmatrix}
1 &  0 & 3 \\
2 & -1 & -1 \\
\end{pmatrix}
\Rightarrow A^{T} =
\begin{pmatrix}
1 &  2 \\
0 & -1 \\
3 & -1 \\
\end{pmatrix}
$$


$$ (2) \text{ Jeden Vektor } a =
\begin{pmatrix}
a_1 \\ 
\vdots \\ 
a_n \\ 
\end{pmatrix} 
\in K^{n}
\text{ kann man als Matrix a $\thicksim$ (n,1) auffassen. } $$
$$ \text{Dann ist }
a^{T} =
\begin{pmatrix}
a_1 & \dots & a_n \\
\end{pmatrix}
\text{$\thicksim$ (1,n).} $$


## Defintion 2.2

Sei A $\in K^{m\times n}$ eine Matrix.
$$ \textbf{Zeilenvektoren: } A_{1 \bullet} = 
\begin{pmatrix}
a_{11} \\ 
\vdots \\ 
a_{1n} \\ 
\end{pmatrix}, \text{ } \dots \text{ }, \text{ }
A_{m \bullet} =
\begin{pmatrix}
a_{m1} \\ 
\vdots \\ 
a_{mn} \\ 
\end{pmatrix}
\in K^{n} $$

$$ \textbf{Spaltenvektoren: } A_{\bullet 1} = 
\begin{pmatrix}
a_{11} \\ 
\vdots \\ 
a_{m1} \\ 
\end{pmatrix}, \text{ } \dots \text{ }, \text{ }
A_{\bullet n} =
\begin{pmatrix}
a_{1n} \\ 
\vdots \\ 
a_{mn} \\ 
\end{pmatrix}
\in K^{m} $$


## Bemerkung

Jede Matrix A $\in K^{m\times n}$ kann man auch mit Hilfe ihrer Spalten- und Zeilenvektoren wie folgt angeben werden:
$$ A = (A_{\bullet 1}, \text{ } \dots \text{ }, \text{ } A_{\bullet n})  \text{ Spaltendarstellung von A} $$

$$ A = (A_{1 \bullet}, \text{ } \dots \text{ }, \text{ } A_{m \bullet}) \text{ Zeilendarstellung von A} $$


## Beispiel

$$ A = 
\begin{pmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
\end{pmatrix}
=
\begin{pmatrix}
a_{11} & a_{21} \\
a_{12} & a_{22} \\
a_{13} & a_{23} \\
\end{pmatrix}^T
$$

$$ Spaltenvektoren: \text{ } A_{\bullet 1} = 
\begin{pmatrix}
a_{11} \\
a_{21} \\
\end{pmatrix}, \text{ }
A_{\bullet 2} = 
\begin{pmatrix}
a_{12} \\
a_{22} \\
\end{pmatrix}, \text{ }
A_{\bullet 3} = 
\begin{pmatrix}
a_{13} \\
a_{23} \\
\end{pmatrix} \text{ }
\in K^2 $$

$$ Zeilenvektoren: \text{ } A_{1 \bullet} = 
\begin{pmatrix}
a_{11} \\
a_{12} \\
a_{13} \\
\end{pmatrix}, \text{ }
A_{2 \bullet} = 
\begin{pmatrix}
a_{21} \\
a_{22} \\
a_{23} \\
\end{pmatrix} \text{ }
\in K^3 $$


## Defition 2.3

Eine Matrix A vom Typ (n,n) heißt eine $\textbf{quadratische}$ (n-reihige) Matrix.
Bei einer quadratischen (n-reihigen) Matrix A ~ (n,n) bilden die Einträge
$a_{11} \text{,} \text{ } \dots \text{ } \text{,} \text{ } a_{nn}$ die sogenannte $\textbf{(Haupt-) Diagonale.}$
Eine quadratische Matrix A ~ (n,n) heißt $\textbf{symmetrisch, }$ wenn A = $A^T$.


## Bemerkung

Ist A ~ (n,n) quadratisch, so erhält man $A^T$ druch Spiegelung von A an der Diagonalen.
Es gilt: A = $(a_{ij})$ symmetrisch $\Leftrightarrow$ $a_{ij} = a_{ji}$ für alle i,j


## Lemma 2.4

Für das Transponieren gelten folgende Rechenregeln:
$$ (1) \text{ } (A+B)^T = A^T + B^T $$
$$ (2) \text{ } (\alpha \cdot A)^T = \alpha \cdot A^T $$
$$ (3) \text{ } (A^T)^T = A $$
$$ (4) \text{ } (A^T)_{j \bullet} = A_{\bullet j} \text{ und } (A^T)_{\bullet i} = A_{i \bullet} $$

Beweis:

$$ (1) \text{ } (A+B)^T = (a_{ij} + b_{ij})^T
= (a_{ji} + b_{ji})
= (a_{ji}) + (b_{ji})
= (a_{ij})^T + (b_{ij})^T
= A^T + B^T $$

(2) und (3) analog, (4) klar nach Definition


## Bemerkung

Seien A ~ (m,n) und B ~ (n,r) Matrizen. Nach 1.8 definieren A und B lineare Abbildungen $A: \  K^n \  \rightarrow \  K^m \text{ und } B:  \  K^r \ \rightarrow \  K^n \text{.}$ Betrachte die Komposition dieser beiden Abbildungen. Kann diese Komposition durch eine Matrix C ~ (m,r) dargestellt werden?

$$
\xymatrix{K^r \ar[r]^B \ar[dr]_C & K^n \ar[d]^A \\
                                 & K^m }
$$



$$
\begin{pmatrix}
x_1 \\
\vdots \\
x_r \\
\end{pmatrix}
\xmapsto{B}
\begin{pmatrix}
y_1 \\
\vdots \\
y_n \\
\end{pmatrix}
\xmapsto{A}
\begin{pmatrix}
z_1 \\
\vdots \\
z_m \\
\end{pmatrix}
$$


$$ B \cdot x =
\begin{pmatrix}
b_{11} & \dots & b_{1r} \\
\vdots &       & \vdots \\
b_{n1} & \dots & b_{nr} \\
\end{pmatrix}
\cdot
\begin{pmatrix}
x_1 \\
\vdots \\
x_r \\
\end{pmatrix}
=
\begin{pmatrix}
\sum\limits_{k=1}^r b_{1k} \cdot x_k \\
\vdots \\
\sum\limits_{k=1}^r b_{nk} \cdot x_k \\
\end{pmatrix}
=
\begin{pmatrix}
y_1 \\
\vdots \\
y_n \\
\end{pmatrix}
$$

$$ A \cdot y =
\begin{pmatrix}
a_{11} & \dots & a_{1n} \\
\vdots &       & \vdots \\
a_{m1} & \dots & b_{mn} \\
\end{pmatrix}
\cdot
\begin{pmatrix}
y_1 \\
\vdots \\
y_n \\
\end{pmatrix}
=
\begin{pmatrix}
\sum\limits_{j=1}^n a_{1j} \cdot y_j \\
\vdots \\
\sum\limits_{j=1}^n b_{mj} \cdot y_j \\
\end{pmatrix}
=
\begin{pmatrix}
z_1 \\
\vdots \\
z_m \\
\end{pmatrix}
$$

$$ C \cdot x =
\begin{pmatrix}
c_{11} & \dots & c_{1r} \\
\vdots &       & \vdots \\
c_{m1} & \dots & b_{mr} \\
\end{pmatrix}
\cdot
\begin{pmatrix}
x_1 \\
\vdots \\
x_r \\
\end{pmatrix}
=
\begin{pmatrix}
\sum\limits_{i=1}^r c_{1i} \cdot x_i \\
\vdots \\
\sum\limits_{i=1}^r c_{mi} \cdot x_i \\
\end{pmatrix}
=
\begin{pmatrix}
z_1 \\
\vdots \\
z_m \\
\end{pmatrix}
$$

Daher folgt: $$ z_i = \sum\limits_{j=1}^n a_{ij} \cdot y_j
= \sum\limits_{j=1}^n a_{ij} \cdot (\sum\limits_{k=1}^r b_{jk} \cdot x_k)
= \sum\limits_{j=1}^n \sum\limits_{k=1}^r a_{ij} \cdot b_{jk} \cdot x_k
= \sum\limits_{k=1}^r (\sum\limits_{j=1}^n a_{ij} \cdot b_{jk}) \cdot x_k $$
$$ \text{Also } z_i = \sum\limits_{k=1}^r c_{ik} \cdot x_k $$.
$$ \text{Insgesamt folgt: } c_{ik} = \sum\limits_{j=1}^n a_{ij} \cdot b_{jk} ( i = 1, ... , m, k = 1, ... , r). $$


## Bemerkung

$$ (1) \  A \cdot B = A \cdot (B_{\bullet 1} \dots B_{\bullet r}) 
= (A \cdot B_{\bullet 1} \dots A \cdot B_{\bullet r}) $$

$$ (2) \text{ Jeder Vektor } a = 
\begin{pmatrix}
a_1 \\
\vdots \\
a_n \\
\end{pmatrix}
\text{ kann als Matrix vom Typ (n,1) aufgefasst werden, die Transponierte }$$ $$a^T = 
\begin{pmatrix}
a_1 & \dots & a_n \\
\end{pmatrix}
\text{ von a als Matrix vom Typ (1,n). Es gibt zwei mögliche Produkte:} $$

$$ \bullet \ a^T \cdot b 
= \begin{pmatrix}
a_1 \dots a_n \\
\end{pmatrix}
\cdot
\begin{pmatrix}
b_1 \\
\vdots \\
b_n \\
\end{pmatrix}
= a_1 \cdot b_1 + \dots + a_n \cdot b_n
= \sum\limits_{i=1}^n a_i \cdot b_i \in K^{1\times 1}
\text{ heißt } \textbf{Standard-Skalarprodukt} \text{ aus } K^n \text{.} $$

$$ \bullet \ a \cdot b^T 
= \begin{pmatrix}
a_1 \\
\vdots \\
a_n \\
\end{pmatrix}
\cdot
\begin{pmatrix}
b_1 & \dots & b_n \\
\end{pmatrix}
= \begin{pmatrix}
a_1 \cdot b_1 & \dots & a_1 \cdot b_n \\
\vdots        &       & \vdots \\
a_n \cdot b_1 & \dots & a_n \cdot b_n \\
\end{pmatrix} \in K^{n\times n} 
\text{ heißt } \textbf{Dyadisches Produkt} \text{ aus } K^n \text{.} $$


## Bemerkung

Das Produkt zweier n-reihiger quadratischer Matrizen A und B ist immer definiert, aber das Kommutativgesetzt ($A \cdot B = B \cdot A$) gilt im Allgemeinen nicht.


## Beispiel


$$\begin{pmatrix}
1&0 \\
0&0 \\
\end{pmatrix}
\cdot
\begin{pmatrix}
0&1 \\
0&0 \\
\end{pmatrix}
= 
\begin{pmatrix}
0&1 \\
0&0 \\
\end{pmatrix}
\neq
\begin{pmatrix}
0&0 \\
0&0 \\
\end{pmatrix}
=
\begin{pmatrix}
0&1 \\
0&0 \\
\end{pmatrix}
\cdot
\begin{pmatrix}
1&0 \\
0&0 \\
\end{pmatrix}$$

Achtung: Die Nullmatrix kann das Ergebnis der Maltrizenmultiplikation von $A \neq 0 \text{ und } B \neq 0$ sein!


## Lemma 2.6

$\text{Seien } A_1, \ A_2 \in K^{m\times n}, \ B_1, \ B_2 \in K^{n\times r}, \ C \in K^{r\times s}, \ \alpha \in K.$
Dann gelten folgende Rechenregeln:

$(1) \text{ Distributivgesestze}$
$$(a) \  A_1 \cdot (B_1 + B_2) = A_1 \cdot B_1 + A_1 \cdot B_2 \text{ und } (A_1 + A_2) \cdot B_1 = A_1 \cdot B_1 + A_2 \cdot B_1$$
$$(b) \ A_1 \cdot ( \alpha \cdot B_1) = (\alpha \cdot A_1) \cdot B_1 = \alpha \cdot ( A_1 \cdot B_1)$$

$(2) \text{ Assoziativgesetz}$
$$\text{Ist eines der Produkte } (A \cdot B) \cdot C, \ A \cdot (B \cdot C) \text{ definiert, so auch das andere und es gilt: } (A \cdot B) \cdot C = \ A \cdot (B \cdot C)$$

$$(3) \ (A \cdot B)^T = B^T \cdot A^T$$

$$(4) \ A \cdot I_n = A = I_n \cdot A \text{ für } A \in K^{n\times n} \text{ mit } I_n = \begin{pmatrix}
1 &        & 0 \\
  & \ddots & \\
0 &        & 1 \\
\end{pmatrix}
\in K^{n\times n} \textbf{ Einheitsmatrix.}$$


## Bemerkung

Es gelten keine Kürzungsregeln:
$$\bullet \ A \cdot B = 0 \nRightarrow A = 0 \text{ oder } D = 0$$
$$\bullet \ A \cdot B = A \cdot C \nRightarrow B = C$$


## Beispiel

$$A = \begin{pmatrix}
0&1\\
0&2\\
\end{pmatrix}, \ 
B = \begin{pmatrix}
1&1\\
3&4\\
\end{pmatrix}, \ 
C = \begin{pmatrix}
2&3\\
3&4\\
\end{pmatrix}, \ 
D = \begin{pmatrix}
3&7\\
0&0\\
\end{pmatrix}$$


## Definition 2.7

Eine quadratische Matrix $A = (a_{ij}) \in K^{n\times n}$ heitßt...

$$\textbf{ obere Dreiecksmatrix, } \text{wenn } a_{ij} = 0 \text{ für alle i > j:}$$
$$\begin{pmatrix}
a_{11} & \dots  & a_{1n} \\
       & \ddots & \vdots \\
0      &        & a_{nn} \\
\end{pmatrix}$$

$$\textbf{ untere Dreiecksmatrix, } \text{wenn } a_{ij} = 0 \text{ für alle i < j:}$$
$$\begin{pmatrix}
a_{11} &        & 0 \\
\vdots & \ddots & \\
a_{n1} & \dots  & a_{nn} \\
\end{pmatrix}$$

$$\textbf{ Diagonalmatrix, } \text{wenn } a_{ij} = 0 \text{ für alle } i \neq j:$$
$$\begin{pmatrix}
a_{11} &        & 0 \\
       & \ddots &  \\
0      &        & a_{nn} \\
\end{pmatrix}$$
$$\text{kurz: diag(} a_{11}, \ ... \ , \ a_{nn} \text{)}$$


## Lemma 2.8

Das Produkt zweier oberer (bzw. unterer) Dreiecksmatrizen ist eine obere (bzw. untere) Dreiecksmatrix. Das Produkt zweier Diagonalmatrizen ist eine Diagnonalmatrix.


## Definiton 2.9

Sei $A = (a_{ij})$ ~ (n,n) eine quadratische Matrix. Dann heißt $tr(A) = \sum\limits_{i=1}^n a_{ii}$ die $\textbf{Spur}$ von A ($\rightarrow$ trace).


## Beispiel

$$tr \begin{pmatrix}
2&3&6\\
4&1&7\\
2&9&3\\
\end{pmatrix}
= 2+1+3 = 6$$


## Satz 2.10

Seien A, B ~ (n,n) quadratische Matrizen und sei $\alpha \in K.$ Dann gilt:
$$(1) \ tr(A+B) = tr(A) + tr(B)$$
$$(2) \ tr(\alpha \cdot A) = \alpha \cdot tr(A)$$
$$(3) \ tr(A^T) = tr(A)$$

Seien A ~ (m,n) und B ~ (n,m) Matrizen. Dann sind $A \cdot B$ und $B \cdot A$ quadratische Matrizen und es gilt: $tr(A \cdot B) = tr(B \cdot A).$

## Beweis:

(1), (2), (3) sind klar.

(4) Sei A = $(a_{ij})$ und B = $(b_{ij}).$ Dann gilt: $$tr(A \cdot B) = \sum\limits_{i=1}^m \sum\limits_{k=1}^n a_{ik} \cdot b_{ki} = \sum\limits_{k=1}^n \sum\limits_{i=1}^m b_{ki} \cdot a_{ik} = tr(B \cdot A)$$


## Folgerung

Sind A, B, C Matrizen, sodass $A \cdot B \cdot C$ definiert und quadratisch ist, so sind auch $B \cdot C \cdot A$ und $C \cdot A \cdot B$ definiert und quadratisch und es gilt: tr($A \cdot B \cdot C$) = tr($B \cdot C \cdot A$) = tr($C \cdot A \cdot B$).


## Definition 2.11

Für i, j $\in \mathbb{N}$ versteht man unter $\textbf{Kronecker-Delta}$ die Zahl $\\$
$\delta_{ij} = \begin{cases}
1 \text{ wenn i = j} \\
0 \text{ wenn } i \neq j \\
\end{cases}$


## Beispiel

Sei $I_{n}$ ~ (n,n) die Einheitsmatrix. Dann gilt: $I_{n}$ = ($\delta_{ij}$) ~ (n,n).


## Definition 2.12

Eine Matrix kann man durch Einfügen von horizontalen und vertikalen Trennungslinien in Untermatrizen zerlegen. Man nennt eine solche Zerlegung eine $\textbf{Partitionierung}$ der Matrix und bezeichnet die Matrix dann als eine $\textbf{partitionierte Matrix}$. Die Untermatrizen einer partitionierten Matrix bezeichnet man als $\textbf{Blöcke}$.


## Beispiel

$$A = \begin{pmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33} \\
\end{pmatrix}
= 
\begin{pmatrix}
A_{11} & A_{12} \\
A_{21} & A_{22} \\
\end{pmatrix}
\text{ mit } A_{11} \sim (2,3), \  A_{12} \sim (2,1), \  A_{21} \sim (1,3), \  A_{22} \sim (1,1)$$

$$A = \begin{pmatrix}
a_{11} & a_{12} & a_{13} & a_{14} \\
a_{21} & a_{22} & a_{23} & a_{24} \\
a_{31} & a_{32} & a_{33} & a_{34} \\
\end{pmatrix}
= 
\begin{pmatrix}
r_1 \\
r_2 \\
r_3 \\
\end{pmatrix}
\text{ mit } r_i \sim (1,4)$$

$$A = \begin{pmatrix}
a_{11} & a_{12} & a_{13} & a_{14} \\
a_{21} & a_{22} & a_{23} & a_{24} \\
a_{31} & a_{32} & a_{33} & a_{34} \\
\end{pmatrix}
=
\begin{pmatrix}
c_1 & c_2 & c_3 & c_4 \\
\end{pmatrix}
\text{ mit } c_i \sim (3,1)$$


## Lemma 2.13

Seien A, B ~ (m,n) partitionierte Matrizen mit derselben Partitionierung, d.h. $A = \begin{pmatrix}
A_{11} & A_{12} \\
A_{21} & A_{22} \\
\end{pmatrix}$
und $B = \begin{pmatrix}
B_{11} & B_{12} \\
B_{21} & B_{22} \\
\end{pmatrix}$
mit $A_{11} \sim (m_1,n_1) \sim B_{11}$, $A_{22} \sim (m_2,n_2) \sim B_{22}$, $A_{12} \sim (m_1,n_2) \sim B_{12}$, $A_{21} \sim (m_2,n_1) \sim B_{21}$, $m_1+m_2=m$ und $n_1+n_2=n$. Dann gilt:

$$\bullet A+B = \begin{pmatrix}
A_{11}+B_{11} & A_{12}+B_{12} \\
A_{21}+B_{21} & A_{22}+B_{22} \\
\end{pmatrix}$$

$$\bullet \alpha \cdot A = \begin{pmatrix}
\alpha \cdot A_{11} & \alpha \cdot A_{12} \\
\alpha \cdot A_{12} & \alpha \cdot A_{22} \\
\end{pmatrix}$$


## Lemma 2.14: Multiplikation und Transponierte

Seien A ~ (m,n) und C ~ (n,p) partitionierte Matrizen mit $\\$
$$\bullet A = \begin{pmatrix}
A_{11} & A_{12} \\
A_{21} & A_{22} \\
\end{pmatrix}$$
$$\ \text{ mit } A_{11} \sim (m_1,n_1), \ A_{22} \sim (m_2,n_2), \ A_{12} \sim (m_1,n_2), \ A_{21} \sim (m_2,n_1), \ m_1+m_2=m, \ n_1+n_2=n.$$
$$\bullet C = \begin{pmatrix}
C_{11} & C_{12} \\
C_{21} & C_{22} \\
\end{pmatrix}$$
$$\ \text{ mit } C_{11} \sim (n_1,p_1), \ C_{22} \sim (n_2,p_2), \ C_{12} \sim (n_1,p_2), \ C_{21} \sim (n_2,p_1), \ n_1+n_2=n, p_1+p_2=p.$$
Dann gilt:

$$\bullet A \cdot C = \begin{pmatrix}
A_{11} \cdot C_{11} + A_{12} \cdot C_{21} & A_{11} \cdot C_{12} + A_{12} \cdot C{22} \\
A_{21} \cdot C_{11} + A_{22} \cdot C_{21} & A_{21} \cdot C_{12} + A_{22} \cdot C_{22} \\
\end{pmatrix}$$

$$\bullet A^T = \begin{pmatrix}
A_{11}^T & A_{21}^T \\
A_{12}^T & A_{22}^T \\
\end{pmatrix}$$

$\\$

Was bedeutet es, wenn f: $K^n \rightarrow K^n$ (bzw. $A \in K^{n \times n}$) ein Isomorphismus ist? $\\$

Es gibt eine lineare Abbildung $f^{-1}: K^n \rightarrow K^n$ (bzw. $\tilde{A} \in K^{n \times n}$) mit $\\ f^{-1} \circ f = Id_{K^n} = f \circ f^{-1}$ (bzw. $\tilde{A} \cdot A = I_n = A \cdot \tilde{A}$).


## Definiton 2.15

Eine quadratische Matrix $A \in K^{n \times n}$ heißt $\textbf{invertierbar,}$ wenn es eine Matrix $\tilde{A} \in K^{n \times n}$ gibt, sodass $A \cdot \tilde{A} = I_n = \tilde{A} \cdot A.$


## Lemma 2.16

Ist A ~ (n,n) invertierbar, so ist $\tilde{A}$ ~ (n,n) mit $A \cdot \tilde{A} = I_n = \tilde{A} \cdot A$ eindeutig bestimmt.

Beweis: $\\$
Sei $A \cdot \tilde{A} = I_n = \tilde{A} \cdot A$ und B eine weitere Matrix mit $A \cdot B = I_n = B \cdot A.$ Dann gilt: $\\$
$$B = B \cdot I_n = B \cdot (A \cdot \tilde{A}) = (B \cdot A) \cdot \tilde{A} = I_n \cdot \tilde{A} = \tilde{A}$$


## Definition 2.17

Sei A ~ (n,n) invertierbar. Dann heißt die eindeutig bestimmte Matrix $\tilde{A}$ ~ (n,n) mit $A \cdot \tilde{A} = I_n = \tilde{A} \cdot A$ die $\textbf{Inverse}$ von A. Sie wird mit $A^{-1}$ bezeichnet.


## Lemma 2.18

Seinen A, B ~ (n,n) invertierbare Matrizen. Dann ist $A \cdot B$ invertierbar und es gilt $(A \cdot B)^{-1} = B^{-1} \cdot A^{-1}.$

Beweis: $\\$
Zz: $B^{-1} \cdot A^{-1}$ hat die Eigenschaft einer Inversen zu $A \cdot B:$ $\\$
$$(A \cdot B) \cdot (B^{-1} \cdot A^{-1}) = A \cdot (B \cdot B^{-1}) \cdot A^{-1} = A \cdot I_n \cdot A^{-1} = A \cdot A^{-1} = I_n$$ $\\$
$$(B^{-1} \cdot A^{-1}) \cdot (A \cdot B) = B^{-1} \cdot (A^{-1} \cdot A) \cdot B = B^{-1} \cdot I_n \cdot B = B^{-1} \cdot B = I_n$$


## Bemerkung
Durch Induktion folgt allgemein: $\\ A_1, \ \dotso \ , \ A_n$ invertierbar $\Rightarrow (A_1 \cdot \dotso \cdot A_n)^{-1} = A_n^{-1} \cdot \dotso \cdot A_1^{-1}$


## Lemma 2.19

Sei $A = \begin{pmatrix}
A_{11} & 0 \\
0      & A_{22} \\
\end{pmatrix},$ wobei $A_{11} \ \sim \ (n_1,n_1)$ und $\ A_{22} \ \sim \ (n_2,n_2)$ invertierbare Matrizen sind. Dann ist A invertierbar und es gilt $A^{-1} = \begin{pmatrix}
A_{11}^{-1} & 0 \\
0         & A_{22}^{-1} \\
\end{pmatrix}.$