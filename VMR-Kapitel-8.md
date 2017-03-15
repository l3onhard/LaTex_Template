#8. Determinanten
Sei $n \in \mathbb{N}$ eine feste Zahl und $N=\{1,...,n\}. \\$
Eine Abbildung $\sigma: N \to N$ kann man angeben durch ihre Wertetabelle $\sigma = \begin{pmatrix} 1 & 2 & ... & n \\ \sigma(1) & \sigma(2) & ... & \sigma(n) \end{pmatrix} \\$
Dabei sind die zugeordneten Zahlen $\sigma(k)$ wieder aus $N$. Wann ist $\sigma$ bijektiv? Wenn in der unteren Reihe der Wertetabelle jede Zahl aus $N$ genau einmal vorkommt.

##Definition 8.1
Eine bijektive Abbildung $\sigma: N \to N$ mit $N=\{1,...,n\}$ heißt Permutation. Die Menge aller Permutationen der Zahlen 1 bis $n$ wird mit $\gamma_n$ bezeichnet. Die Komposition von Abbildungen definiert eine innere Verknüpfung $\circ$ auf $\gamma_n: \\
\sigma, \tau \in \gamma_n \implies \sigma \circ \tau \in \gamma_n$ mit $\sigma \circ \tau (j) = \sigma (\tau (j))$ für $j \in N \\$
Es gilt natürlich das Assoziativgesetz: $\\
(\sigma \circ \tau) \circ \mu = \sigma \circ (\tau \circ \mu)\\$
Weiter gibt es ein "neutrales Element" $\iota = \begin{pmatrix} 1 & 2 & ... & n \\ 1 & 2 & ... & n \end{pmatrix} (\equiv$ Identität auf $N$) mit $\sigma \circ \iota = \sigma = \iota \circ \sigma \forall \sigma \in \gamma_n. \\$
Ist $\sigma \in \gamma_n,$ so ist $\sigma: N \to N$ bijektiv und es existiert Umkehrabbildung $\sigma^{-1}:N \to N$, die ebenfalls bijektiv ist.
Daher ist $\sigma^{-1} \in \gamma_n$ mit $\sigma^{-1} \circ \sigma = \iota = \sigma \circ \sigma^{-1}.$

##Folgerung
$(\gamma_n, \circ)$ ist eine Gruppe. Sie heißt die symmetrische Gruppe (zur Zahl $n$).

###Bemerkung
Für $n \geq 3$ ist $\gamma_n$ nicht kommutativ.

###Beispiel
$\sigma = \begin{pmatrix} 1 & 2 & 3 \\ 3 & 1 & 2 \end{pmatrix}$ und $\tau = \begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 2 \end{pmatrix} \\
\sigma \circ \tau = \begin{pmatrix} 1 & 2 & 3 \\ 3 & 2 & 1 \end{pmatrix} \neq \begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 3 \end{pmatrix} = \tau \circ \sigma \\$
Weiter ist $\sigma^{-1} = \begin{pmatrix} 1 & 2 & 3 \\ 2 & 3 & 1 \end{pmatrix}$ und $\tau^{-1} = \begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 2 \end{pmatrix} = \tau$

###Bemerkung
In der unteren Zeile einer Permutation $\sigma = \begin{pmatrix} 1 & ... & n \\ \sigma(1) & ... & \sigma(n) \end{pmatrix}$ kann man durch Vertauschungen jeweils benachbarter Zahlen erreichen, dass die Zahlen dann in der natürlichen Reihenfolge hintereinander stehen. Gleichgültig, wie man dabei vorgeht, benötigt man für eine Permutation $\sigma$ immer eine gerade Anzahl von Vertauschungen. Dementsprechend spricht man von geraden bzw. ungeraden Permutationen und ordnet jeder Permutation ein Vorzeichen zu: das Vorzeichen + der geraden und das Worzeichen - der ungeraden Permutationen. Um das Vorzeichen zu bestimmen, definieren wir für jede Permutation $\sigma = \begin{pmatrix} 1 & ... & n \\ \sigma(1) & ... & \sigma(n) \end{pmatrix}$ die folgenden Anzahlen: $\\
\Phi_1 (\sigma)=$ Anzahl der Zahlen in $\sigma(1),...,\sigma(n)$ links von 1 $\\
\Phi_2 (\sigma)=$ Anzahl der Zahlen in $\sigma(1),...,\sigma(n)$ links von 2 und $>2 \\
\vdots \\
\Phi_{n-1} (\sigma)=$ Anzahl der Zahlen in $\sigma(1),...,\sigma(n)$ von $n-1$ und $>n-1 \\$
Dann gilt: Die Summe $\Phi(\sigma)=\Phi_1(\sigma)+\Phi_2(\sigma)+...+\Phi_{n-1}(\sigma)$ ist die Anzahl der Nachbarvertauschungen, die nötig sind, um zuerst 1 nach links an ihren Platz, dann 2 nach links an ihren Platz usw. zu bringen, sodass schließlich dei Reihenfolge $1,2,...,n$ hergestellt ist.

##Definition 8.2
Für eine Permutation $\sigma \in \gamma_n$ heißt $\Phi(\sigma)$ die Fehlstandszahl von $\sigma$ und $sgn(\sigma):=(-1)^{\Phi(\sigma)}$ das Vorzeichen von $\sigma. \\$
Eine Permutation $\sigma$ heißt gerade (bzw. ungerade), wenn $\Phi(\sigma)$ gerade (bzw. ungerade) ist.

###Beispiel
$\sigma = \begin{pmatrix} 1 & 2 & 3 & 4 \\ 3 & 4 & 2 &1 \end{pmatrix} \\
\Phi_1(\sigma)=3,\Phi_2(\sigma)=2, \Phi_3(\sigma)=0 \\
\implies \Phi(\sigma)=5$ ist ungerade $\\
\implies sgn(\sigma)= (-1)^5 = -1$

##Lemma 8.3
Für $\sigma, \tau \in \gamma_n$ gilt:

(1) $sgn(\sigma \circ \tau) = sgn(\sigma) \cdot sgn(\tau)$
(2) $sgn(\sigma) = sgn(\sigma^{-1})$

##Definition 8.4
Sei $K^{(n,n)}$ der Vektorraum der $n$-reihigen Matrizen, $n \in \mathbb{N}. \\$
Die Determinantenfunktion $det: K^{(n,n)} \to K$ ordnet jeder Matrix $A \in K^{(n,n)}$ eine Zahl aus $K$ zu, die die Determinante von $A$ ist und wie folgt bezeichnet wird: $\\
A = \begin{pmatrix} a_{11} & ... & a_{1n} \\ a_{n1} & ... & a_{nn} \end{pmatrix} \to det(A) = \begin{vmatrix} a_{11} & ... & a_{1n} \\ a_{n1} & ... & a_{nn} \end{vmatrix} \\$
Dabei ist $det(A) \sum\limits_{\sigma \in \gamma_n} sgn(\sigma) \cdot a_{1\sigma(1)} \cdot ... \cdot a_{n\sigma(n)}$

Berechnung der 2- und 3-reihigen Dterminanten:

(1) $n=2 \\
A = \begin{pmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{pmatrix} \implies det(A) = a_{11} \cdot a_{22} - a_{12} \cdot a_{21} \\$
Denn: $N=\{1,2\} \to \gamma_2 = \{ \tau= \begin{pmatrix} 1 & 2 \\ 1 & 2 \end{pmatrix} , \sigma = \begin{pmatrix} 1 & 2 \\ 2 & 1 \end{pmatrix} \}$ mit $sgn(\tau)= (-1)^0 = 1$ und $sgn(\sigma) = (-1)^1 = -1 \\$
(2) $n=3 \\
A = \begin{pmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{pmatrix} \\$


$$
\begin{tabular}{c|c c c c c c}
Permutationen &
$\begin{pmatrix} 1 & 2 & 3 \\ 1 & 2 & 3 \end{pmatrix}$ &
$\begin{pmatrix} 1 & 2 & 3 \\ 2 & 3 & 1 \end{pmatrix}$ &
$\begin{pmatrix} 1 & 2 & 3 \\ 3 & 1 & 2 \end{pmatrix}$ &
$\begin{pmatrix} 1 & 2 & 3 \\ 3 & 2 & 1 \end{pmatrix}$ &
$\begin{pmatrix} 1 & 2 & 3 \\ 2 & 1 & 3 \end{pmatrix}$ &
$\begin{pmatrix} 1 & 2 & 3 \\ 1 & 3 & 2 \end{pmatrix}$ \\
$\Phi(\sigma)$ &
0 &
2 &
2 &
3 &
1 &
1 \\
$sgn(\sigma)$ &
1 &
1 &
1 &
-1 &
-1 &
-1
\end{tabular} $$

$\implies det(A) = a_{11} \cdot a_{22} \cdot a_{33} + a_{12} \cdot a_{23} \cdot a_{31} + a_{13} \cdot a_{21} \cdot a_{32} - a_{13} \cdot a_{22} \cdot a_{31} - a_{12} \cdot a_{21} \cdot a_{33} - a_{11} \cdot a_{23} \cdot a_{32}$


Merkregel: Regel von Sarus
\begin{tikzpicture}
     \matrix [%
       matrix of math nodes,
       column sep=1em,
       row sep=1em
     ] (sarrus) {%
       a_{11} & a_{12} & a_{13} & a_{11} & a_{12} \\
       a_{21} & a_{22} & a_{23} & a_{21} & a_{22} \\
       a_{31} & a_{32} & a_{33} & a_{31} & a_{32} \\
     }; 
 
     \path ($(sarrus-1-3.north east)+(0.5em,0)$) edge[dotted] ($(sarrus-3-3.south east)+(0.5em,0)$)
           (sarrus-1-1)                          edge         (sarrus-2-2)
           (sarrus-2-2)                          edge         (sarrus-3-3)
           (sarrus-1-2)                          edge         (sarrus-2-3)
           (sarrus-2-3)                          edge         (sarrus-3-4)
           (sarrus-1-3)                          edge         (sarrus-2-4)
           (sarrus-2-4)                          edge         (sarrus-3-5)
           (sarrus-3-1)                          edge[dashed] (sarrus-2-2)
           (sarrus-2-2)                          edge[dashed] (sarrus-1-3)
           (sarrus-3-2)                          edge[dashed] (sarrus-2-3)
           (sarrus-2-3)                          edge[dashed] (sarrus-1-4)
           (sarrus-3-3)                          edge[dashed] (sarrus-2-4)
           (sarrus-2-4)                          edge[dashed] (sarrus-1-5);
 
     \foreach \c in {1,2,3} {\node[anchor=south] at (sarrus-1-\c.north) {$+$};};
     \foreach \c in {1,2,3} {\node[anchor=north] at (sarrus-3-\c.south) {$-$};};
   \end{tikzpicture}


###Beispiele
(1) $det \begin{pmatrix} 3 & 1 \\ 4 & -2 \end{pmatrix} = 3\cdot (-2) - 1 \cdot 4= -10 \\$
(2) $det \begin{pmatrix} 1 & 2 & 3 \\ -4 & 5 & 6 \\ 7 & -8 & 9 \end{pmatrix} = 1 \cdot 5 \cdot 9 + 2 \cdot 6 \cdot 7+ 3 \cdot (-4) \cdot (-8) - 3 \cdot 5 \cdot 7 - 1 \cdot 6 \cdot (-8) - 2 \cdot (-4) \cdot 9 =45+84+96-105+48+72 = 240$

###Bemerkung
Analoge Rechen- und Merkregeln wie in diesen Fällen ($n=2$ und $n=3$) gibt es für $n \geq 4$ nicht!