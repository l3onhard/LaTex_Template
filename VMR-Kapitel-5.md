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

$$
\begin{aligned}
\mathbb{L}(A, b) &= f^{-1}(b)\ \text{(Menge der Urbilder von b unter f)} \\
\mathbb{L}(A, 0) &= Ker f
\end{aligned}
$$

### Beispiel

$$
\begin{aligned}
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
\end{aligned}
$$

## Satz 5.2

Gegeben sei das LGS $A \cdot x=b$, wobei $A \sim (m,n)$. Sei $r$ der Spaltenrang von $A$, d.h. $r = dim(SR(A))$. Dann gilt:

1) $\mathbb{L}(A,0) \subseteq K^n$ ist $(n-r)$-dimensionaler UVR
2) $\mathbb{L} = \emptyset$ oder $\mathbb{L}(A,b)$ hat folgende Form:
$$\mathbb{L}(A,b) = v + \mathbb{L}(A,0) \text{ , wobei } v \in \mathbb{L}(A,b) \text{ eine beliebige Lösung ist}$$

### Beweis

(1) Sei $f: K^n \to K^m$ die durch A definierte lineare Abbildung mit $f(x) = A \cdot x$. Die Spalten von $A$ sind genau die Bilder $f(e_j)$ der Standardbasisvektoren: $f(e_j) = A \cdot e_j = A_{\cdot j}$. \newline Daher sind die Spaltenvektoren von $A$ ein EZS von $Im(f)$, d.h. es gilt $Im(f) = SR(A)$. Daraus folgt $dim(Im(f)) = r$. \newline Mit der Dimensionsformel (siehe 6.2) folgt:
$$
dim(K^n) = dim(Ker(f)) + dim(Im(f)) \iff n = dim(Ker(f)) + r
$$ \newline
Daraus folgt: $dim(Ker(f)) = n - r$. \newline Da $Ker(f) = \mathbb{L}(A,0) \subseteq K^n$ ist UVR mit $dim(\mathbb{L}(A,0)) = n-r$.

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
$$
\begin{aligned} \mathbb{L}(A,b) \neq \emptyset &\iff \exists v \in K^n \ \text{mit} \ A \cdot v = b \\
& \iff v_1 \cdot A_{\bullet 1} + \dots + v_n \cdot A_{\bullet n} = b \\
& \iff b \text{ ist Linearkombination der Spalten von } A \\
& \iff b \text{ ist Linearkombination der } r \text{ linear unabhängigen Spalten von } A \\
& \iff Rg((A|b)) = r
\end{aligned}
$$

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

Dann gilt:

(1) Ist $b_i \neq 0$ für ein $i$ mit $r + 1 \leq i \leq m$, so hat das LGS keine Lösung, da $0 \cdot x_1 + \ldots + 0 \cdot x_n = b_i \neq 0$ durch kein n-Tuple $(x_1, \ldots , x_n)$ erfüllbar ist.
(2) Seien $b_{r+1} = \ldots = b_m = 0$. Dann hat das LGS Lösungen, die man wie folgt erhält: \newline
Wir setzen $k = n - r$ und wählen für die Unbekannten $x_{r+1}, \ldots, x_n$ Parameter $\lambda_1, \ldots, \lambda_k$, d.h. setze $x_{r+1} = \lambda_1, \ldots, x_n = \lambda_k$.
Die Parameter dürfen unabhängig voneinander beliebige Werte annehmen.
Die übrigen Variablen $x_1, \ldots, x_r$ kann man nun eindeutig in Abhängigkeit vo den Parametern berechnen.
Das geschieht wie folgt: \newline
$r$-te Gleichung: $a_{rr} \cdot x_r + a_{rr+1} \cdot \lambda_1 + \ldots + a_{rn} \cdot \lambda_k = b_r$ \newline
$a_{rr} \neq 0 \implies x_r = \frac{1}{a_{rr}} \cdot (b_r - a_{rr_1} \cdot \lambda_1 - \ldots - a_{rn} \cdot \lambda_k)$ \newline
Man setzt $x_r$ in die $(r-1)$-te Gleichung ein und berechnet man aus der ersten Gleichung $x_1$.
(3) Ist $r = m$, so kann man keinen Parameter einführen.
Es gibt dann eine einzige Lösung $(x_1, \ldots, x_n)$, d.h. das LGS ist dann eindeutig lösbar.

### Beispiel

$$
\begin{aligned}
(A|b) =
\begin{pmatrix}
0 & 2 & 0 & 4 & 6 & 0 & 5 & \BAR & 3 \\
0 & 0 & 1 & 3 & 2 & 1 & 0 & \BAR & 1 \\
0 & 0 & 0 & 0 & 0 & 3 & 1 & \BAR & 2 \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & \BAR & 0
\end{pmatrix}
\begin{pmatrix}
2 & 0 & 0 & 5 & 6 & 4 & 0 & \BAR & 3 \\
0 & 1 & 1 & 0 & 2 & 3 & 0 & \BAR & 1 \\
0 & 0 & 3 & 1 & 0 & 0 & 0 & \BAR & 2 \\
0 & 0 & 0 & 0 & 0 & 0 & 0 & \BAR & 0
\end{pmatrix}
\end{aligned}
$$

$$
A=
\begin{blockarray}{c@{\hspace{5pt}}rr@{\hspace{5pt}}cl}
    0 & 2 & 0 & 4 & 6 & 0 & 5 & \BAR & 3 \\
    0 & 0 & 1 & 3 & 2 & 1 & 0 & \BAR & 1 \\
    0 & 0 & 0 & 0 & 0 & 3 & 1 & \BAR & 2 \\
    0 & 0 & 0 & 0 & 0 & 0 & 0 & \BAR & 0
\end{blockarray}
$$


###hier


$r=3, b_4 = 0 \Rightarrow \mathbb{L}(A,b) \neq \emptyset \\$
Parameter für die Unbekannten $x_1,x_4, x_5, x_7$ wählen:
$\\ x_1 = \lambda_1, x_4 = \lambda_2, x_5 = \lambda_3, x_7 = \lambda_4 \\$

$3.$ Gleichung: $3 \cdot x_6 + \lambda_4 = 2 \Rightarrow x_6 = \frac{2}{3} -\frac{1}{3} \cdot \lambda_4 \\$

$2.$ Gleichung: $x_3 + \frac{2}{3} - \frac{1}{3} \cdot \lambda_4 + 2 \cdot \lambda_3 +3 \cdot \lambda_2 = 1 \Rightarrow x_3 = \frac{1}{3} -3 \cdot \lambda_2 -2 \cdot \lambda_3 + \frac{1}{3} \cdot \lambda_4 \\$

$1.$ Gleichung: $2 \cdot x_2 + 5 \cdot \lambda_4 + 6 \cdot \lambda_3 + 4 \cdot \lambda_2 = 3 \Rightarrow x_2 = 1,5 - 2 \cdot \lambda_2 -3 \cdot \lambda_3 -2,5 \cdot \lambda_4 \\$


$$\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \\ x_5 \\ x_6 \\ x_7 \end{pmatrix} = 
\begin{pmatrix} \lambda_1 \\ 1,5 - 2 \cdot \lambda_2 -3 \cdot \lambda_3 -2,5 \cdot \lambda_4 \\ \frac{1}{3} -3 \cdot \lambda_2 -2 \cdot \lambda_3 + \frac{1}{3} \cdot \lambda_4 \\ \lambda_2 \\ \lambda_3 \\ \frac{2}{3} -\frac{1}{3} \cdot \lambda_4 \\ \lambda_4 \end{pmatrix}$$

$$\begin{pmatrix} x_1 \\ x_2 \\ x_3 \\ x_4 \\ x_5 \\ x_6 \\ x_7 \end{pmatrix} = \underbrace{\begin{pmatrix} 0 \\ 1,5 \\ \frac{1}{3} \\ 0 \\ 0 \\ \frac{2}{3} \\ 0 \end{pmatrix}}_{\text{spezielle Lösung des inhomogenen Systems}} + \underbrace{\lambda_1 \cdot \begin{pmatrix} 1 \\ 0 \\ 0 \\ 0 \\0 \\0 \\0 \end{pmatrix} + \lambda_2 \cdot \begin{pmatrix} 0 \\ -2 \\ -3 \\ 1 \\ 0 \\ 0 \\ 0 \end{pmatrix} + \lambda_3 \cdot \begin{pmatrix}0 \\ -3 \\ -2 \\ 0 \\ 1 \\ 0 \\ 0 \end{pmatrix} + \lambda_4 \cdot \begin{pmatrix} 0 \\ -2,5 \\ \frac{1}{3} \\ 0 \\ 0 \\ -\frac{1}{3} \\ 1 \end{pmatrix}}_{\text{allgemeine Lösung des homogenen Systems}} \\$$ 


## Satz 5.5: Gaußsches Eliminationsverfahren

Sei $(A|b)$ die eweiterte Matrix eins LGS $A \cdot x = b.$ Durch elementare Zeilenumformungen sei $(A|b)$ überführt worden in $(\tilde{A}|\tilde{b}),$ wobei $\tilde{A}$ in Zeilenstufenform ist. Dann haben $(A|b)$ und $(\tilde{A}|\tilde{b})$ dieselben Lösungsräume, d.h. $\mathbb{L}(A,b) = \mathbb{L}(\tilde{A},\tilde{b}).$


## Lemma 5.6

Für eine Matrix $A \in K^{n \times n}$ sind folgende Eigenschaften äquivalent:

(1) A ist invertierbar
(2) $A^T$ ist invertierbar
(3) Spaltenrang(A) = n
(4) Zeilenrang(A) =n

Insbesondere gilt dann: $(A^T)^{-1} = (A^{-1})^T$

Beweis:

$(1) \Rightarrow (2):$ Sei A invertierbar. Dann gilt:
$\\ \bullet A^T \cdot (A^{-1})^T = (A^{-1} \cdot A)^T = I_n^T = I_n.$
$\\ \bullet (A^{-1})^T \cdot A^T = (A \cdot A^{-1})^T = I_n^T = I_n.\\$
Also ist $A^T$ invertierbar und $(A^T)^{-1} = (A^{-1})^T.$

$(2) \Rightarrow (1):$ Sei $A^T$ invertierbar. Dann gilt wegen $"(1) \Rightarrow (2)"$: $(A^T)^T = A$ ist invertierbar.

$\\ (1) \Leftrightarrow (3): \\$
A invertierbar $\Leftrightarrow f_A: K^n \rightarrow K^n$ Isomorphismus
$\Leftrightarrow Ker(f_A) = \{0\}$ und $Im(f_A) = K^n \Leftrightarrow n = dim(Im(f_A)) = Spaltenrang(A) \\$

$(1) \Leftrightarrow (4): \\$
A invertierbar $\Leftrightarrow A^T$ invertierbar $\Leftrightarrow Spaltenrang(A^T) = n \Leftrightarrow Zeilenrang(A) = n \\$