# 7. Koordinatentransformationen


## BEISPIELE

Seien $\mathcal{A} = (e_1 = \begin{pmatrix} 1 \\ 0 \end{pmatrix}, e_2 = \begin{pmatrix} 0 \\ 1 \end{pmatrix}), ~ \mathcal{B} = (v_1 = \begin{pmatrix} 1 \\ 1 \end{pmatrix}, v_2 = \begin{pmatrix} -1 \\ 1 \end{pmatrix})$ Basen von $\mathbb{R}^2$ und sei $\alpha = \begin{pmatrix} 3 \\ 2 \end{pmatrix} \in \mathbb{R}^2.$ Dann gilt: $\alpha = 3 \cdot e_1 + 2 \cdot e_2$ und $\alpha = \frac{5}{2} \cdot v_1 - \frac{1}{2} \cdot v_2. \\$

$\mathcal{B} \rightarrow \mathcal{A}: \ M_{\mathcal{A}}^{\mathcal{B}} (id_V) = \begin{pmatrix} 1 & -1 \\ 1 & 1 \end{pmatrix} \\
\Rightarrow M_{\mathcal{A}}^{\mathcal{B}} (id_V) \cdot \begin{pmatrix} \frac{5}{2} \\ -\frac{1}{2} \end{pmatrix} = \begin{pmatrix} 3 \\ 2 \end{pmatrix} \\$

$\mathcal{A} \rightarrow \mathcal{B}: \ M_{\mathcal{B}}^{\mathcal{A}} (id_V) = (M_{\mathcal{A}}^{\mathcal{B}} (id_V))^{-1} = \begin{pmatrix} 1 & -1 \\ 1 & 1 \end{pmatrix}^{-1} = \begin{pmatrix} \frac{1}{2} & \frac{1}{2} \\ -\frac{1}{2} & \frac{1}{2} \end{pmatrix} \\
\Rightarrow M_{\mathcal{B}}^{\mathcal{A}} (id_V) \cdot \begin{pmatrix} 3 \\ 2 \end{pmatrix} = \begin{pmatrix} \frac{5}{2} \\ -\frac{1}{2} \end{pmatrix} \\$

In einem K-Vektorraum V seien gleichzeitig zwei Basen $\mathcal{A} = (v_1,...,v_n)$ und $\mathcal{B} = (w_1,...,w_n)$ gegeben. Folglich haben wir zwei verschiedene Koordinatensysteme $\Phi_{\mathcal{A}}: K^n \rightarrow V$ mit 
$\Phi_{\mathcal{A}}(e_j) = v_j$ und $\Phi_{\mathcal{B}}: K^n \rightarrow V$ mit $\Phi_{\mathcal{B}}(e_j) = w_j.$ Jeder Vektor v hat eine eindeutige Darstellung bzgl. $\mathcal{A}$ und bzgl. $\mathcal{B}: \\$
$x_1 \cdot v_1 + ... +x_n \cdot v_n = v = y_1 \cdot w_1 + ... + y_n \cdot w_n \\$
Also unterschiedliche Koordinatendarstellung von v bzgl. $\mathcal{A}$ und bzgl. $\mathcal{B}. \\$

Mithilfe der darstellenden Matrix der identischen Abbildung gelangt man von 
$\Phi_{\mathcal{A}}^{-1} (v) = \begin{pmatrix} x_1 \\ \vdots \\ x_n \end{pmatrix}$ nach $\Phi_{\mathcal{B}}^{-1} (v) = \begin{pmatrix} y_1 \\ \vdots \\ y_n \end{pmatrix}.$ Betrachte das folgende Diagramm:

$\xymatrix{
K^n \ar[r]^{\Phi_{\mathcal{A}}} \ar[d]_{M_{\mathcal{B}}^{\mathcal{A}} (id_V)} & V \ar[d]^{id_V} \\
K^n \ar[r]_{\Phi_{\mathcal{B}}} & V } \\$

$M_{\mathcal{B}}^{\mathcal{A}} (id_V) \cdot \begin{pmatrix} x_1 \\ \vdots \\ x_n \end{pmatrix} 
= M_{\mathcal{B}}^{\mathcal{A}} (id_V) \cdot \Phi_{\mathcal{A}}^{-1} (x_1 \cdot v_1 + ... + x_n \cdot v_n)
= M_{\mathcal{B}}^{\mathcal{A}} (id_V) \cdot \Phi_{\mathcal{A}}^{-1} (v) 
= \Phi_{\mathcal{B}}^{-1} (id_V(v)) 
= \Phi_{\mathcal{B}}^{-1} (y_1 \cdot w_1 +...+ y_n \cdot w_n) 
= \begin{pmatrix} y_1 \\ \vdots \\ y_n \end{pmatrix}$


## Bezeichnung

Transformationsmatrix $T_{\mathcal{B}}^{\mathcal{A}}$ anstelle von $M_{\mathcal{B}}^{\mathcal{A}} (id_V)$


## Bemerkung

Wegen der Kommutativität des Diagramms 
$\\ \xymatrix{
K^n \ar[r]^{\Phi_{\mathcal{A}}} \ar[d]_{T_{\mathcal{B}}^{\mathcal{A}}} & V \ar[d]^{id_V} \\
K^n \ar[r]_{\Phi_{\mathcal{B}}} & V } \iff \xymatrix{
K^n \ar[drr]^{\Phi_{\mathcal{A}}} \ar[dd]_{T_{\mathcal{B}}^{\mathcal{A}}} & & \\
 & & V \\
K^n \ar[urr]_{\Phi_{\mathcal{B}}} & &  } \\$

gilt $T_{\mathcal{B}}^{\mathcal{A}} = \Phi_{\mathcal{B}}^{-1} (\Phi_{\mathcal{A}} (\begin{pmatrix} x_1 \\ \vdots \\ x_n \end{pmatrix})) \forall ~ x = \begin{pmatrix} x_1 \\ \vdots \\ x_n \end{pmatrix} \in K^n.$
Nach 6.5 ist daher $T_{\mathcal{B}}^{\mathcal{A}}$ die zu der linearen Abbildung $\Phi_{\mathcal{B}}^{-1} \circ \Phi_{\mathcal{A}}$ gehörende eindeutige Matrix, deren Spalten die Vektoren $\Phi_{\mathcal{B}}^{-1} (\Phi_{\mathcal{A}}(e_j)) = \Phi_{\mathcal{B}}^{-1} (v_j)$ der Koordinatendarstellung der Basisvektoren $v_j \in \mathcal{A}$ bzgl. $\mathcal{B}$ entspricht.


## Satz und Definition 7.1

Sei V ein K-Vektorraum mit $dim_K(V) = n$ und seien $\mathcal{A} = (v_1,...,v_n)$ und $\mathcal{B} = (w_1,...,w_n)$ Basen von V. Die darstellende Matrix $T_{\mathcal{B}}^{\mathcal{A}} \in K^{n \times n}$ der linearen Abbildung $\Phi_{\mathcal{B}}^{-1} \circ \Phi_{\mathcal{A}}: K^n \rightarrow K^n$ bzgl. der Standardbasis $(e_1,...,e_n)$ von $K^n$ heißt die 
$\textbf{Transformationsmatrix}$ für den Basiswechsel von $\mathcal{A}$ nach 
$\mathcal{B}.$ Ihre Spalten sind die Koordinatendarstellung der Basisvektoren $v_j \in \mathcal{A}$ bzgl. der Basis $\mathcal{B}.$ Sie hat die folgende Eigenschaft: Ist $v = x_1 \cdot v_1 +...+ x_n \cdot v_n = y_1 \cdot w_1 +...+ y_n \cdot w_n,$ so gilt $T_{\mathcal{B}}^{\mathcal{A}} \cdot \begin{pmatrix} x_1 \\ \vdots \\ x_n \end{pmatrix} = \begin{pmatrix} y_1 \\ \vdots \\ y_n 
\end{pmatrix}.$


## Bemerkung

Da $\Phi_{\mathcal{B}}^{-1} \circ \Phi_{\mathcal{A}}$ ein Isomorphismus ist, ist $T_{\mathcal{B}}^{\mathcal{A}}$ invertierbar. Natürlich gilt $\\ (T_{\mathcal{B}}^{\mathcal{A}})^{-1} = T_{\mathcal{A}}^{\mathcal{B}}.$


## Anwendungen

$(1)$ Sei $V = K^n$ und seien $\mathcal{A} = (v_1,...,v_n)$ und $\mathcal{B} = (w_1,...,w_n)$ Basen von V. Die Basisvektoren $v_j$ und $w_j$ sind als Spalten gegeben, d.h. sie sind gegeben durch ihre Koordinatendarstellung bzgl. $\mathcal{K}.$ Nach 7.1 gilt: $T_{\mathcal{K}}^{\mathcal{A}} = (v_1,...,v_n)$ und $T_{\mathcal{K}}^{\mathcal{B}} = (w_1,...,w_n). \\$
Diagramm (*: $\\$
$$\xymatrix{
K^n \ar[dd]_{T_{\mathcal{B}}^{\mathcal{A}}} \ar[rd]_{T_{\mathcal{K}}^{\mathcal{A}}} \ar[rrrrd]^{\Phi_{\mathcal{A}}} & & & \\
 & K^n \ar[rrr]^ {\Phi_{\mathcal{K}}=id_{K^n}}  & & & K^n \\
K^n \ar[ru]^{T_{\mathcal{K}}^{\mathcal{B}}} \ar[rrrru]_ {\Phi_{\mathcal{B}}}       & & & } \\$$


Hier sind die Diagramme 1 und 2 kommutativ nach Definition von $T_{\mathcal{K}}^{\mathcal{A}}$ und $T_{\mathcal{K}}^{\mathcal{B}}.$ Das große, äußere Dreieck (*) ist kommutativ nach Definition von $T_{\mathcal{B}}^{\mathcal{A}}.$ Damit folgt, dass auch 3 kommutativ ist:
$\\ \Phi_{\mathcal{B}} \cdot (T_{\mathcal{K}}^{\mathcal{B}})^{-1} \cdot T_{\mathcal{K}}^{\mathcal{A}} \stackrel{(2)}{=} \Phi_{\mathcal{K}} \cdot T_{\mathcal{K}}^{\mathcal{A}} \stackrel{(1)}{=} \Phi_{\mathcal{A}} \stackrel{(*)}{=} \Phi_{\mathcal{B}} \cdot T_{\mathcal{B}}^{\mathcal{A}} \\$
Da $\Phi_{\mathcal{B}}$ Isomorphismus, folgt $T_{\mathcal{B}}^{\mathcal{A}} = (T_{\mathcal{K}}^{\mathcal{B}})^{-1} \cdot T_{\mathcal{K}}^{\mathcal{A}} \\$

$(2)$ Sei V ein beliebiger K-Vektorraum mit gegebener Basis $\mathcal{A} =  (v_1,...,v_n).$ Eine neue Basis $\mathcal{B} = (w_1,...,w_n)$ von V sie gegeben, indem die $w_j$ als Linearkombination der $v_j$ gegeben sind: $w_j = s_{1j} \cdot v_1 +...+ s_{nj} \cdot v_n$ für j = 1,...,n. Sei $S = \begin{pmatrix} s_{11} & \dotso & s_{1n} \\ \vdots & & \vdots \\ s_{n1}& \dotso & s_{nn} \end{pmatrix}$ die Matrix, deren Spalten die Koordinatendarstellung der $w_j \in \mathcal{B}$ bzgl. $\mathcal{A}$ sind: $w_j = s_{1j} \cdot v_1 +...+ s_{nj} \cdot v_n \iff \Phi_{\mathcal{A}}^{-1} (w_j) = \begin{pmatrix} s_{1j} \\ \vdots \\ s_{nj} \end{pmatrix}$ für j = 1,...,n. Nach 7.1 ist dann $S  = T_{\mathcal{A}}^{\mathcal{B}}$ und $T_{\mathcal{B}}^{\mathcal{A}} = (T_{\mathcal{A}}^{\mathcal{B}})^{-1} = S^{-1}.$ Ergebnis: Ist S wie oben angegeben, so ist $T_{\mathcal{A}}^{\mathcal{B}} = S^{-1}$ die Transformationsmatrix für den Basiswechsel von $\mathcal{A}$ nach $\mathcal{B}.$


## Satz 7.2 (Transformationsformel)

Seien V und W K-Vektorräume mit $dim_K(V) = n$ und $dim_K(W) = m.$ Seien $\mathcal{A}, \mathcal{A}'$ Basen von V und $\mathcal{B}, \mathcal{B}'$ Basen von W. Sei $f: V \rightarrow W$ eine lineare Abbildung. Dann ist das folgende Diagramm kommutativ:

$$\\ \xymatrix{
K^n \ar[rrrrrr]^{M_{\mathcal{B}}^{\mathcal{A}}(f)} \ar[dddd]_{T_{\mathcal{A'}}^{\mathcal{A}}} \ar[rrdd]_{\Phi_{\mathcal{A}}} & & & & & & K^m \ar[lldd]^{\Phi_{\mathcal{B}}} \ar[dddd]^{T_{\mathcal{B'}}^{\mathcal{B}}}\\
 & & & \textbf{1} & & & \\
 & \textbf{3} & V \ar[rr]^f & & W & \textbf{4} & \\
 & & & \textbf{2} & & & \\
K^n \ar[rrrrrr]^{M_{\mathcal{B'}}^{\mathcal{A'}}(f)} \ar[rruu]^{\Phi_{\mathcal{A'}}} & & & & & & K^m \ar[lluu]_{\Phi_{\mathcal{B'}}} }$$

Insbesondere gilt: $M_{\mathcal{B'}}^{\mathcal{A'}}(f) = T_{\mathcal{B'}}^{\mathcal{B}} \cdot M_{\mathcal{B}}^{\mathcal{A}}(f) \cdot (T_{\mathcal{A'}}^{\mathcal{A}})^{-1} = T_{\mathcal{B'}}^{\mathcal{B}} \cdot M_{\mathcal{B}}^{\mathcal{A}}(f) \cdot T_{\mathcal{A}}^{\mathcal{A'}} \\$

Beweis: $\\$
Die Diagramme 1 und 2 sind kommutativ nach Definition von $M_{\mathcal{B}}^{\mathcal{A}}(f)$ und $M_{\mathcal{B'}}^{\mathcal{A'}}(f).$ Die Diagramme 3 und 4 sind kommutativ nach Definition von $T_{\mathcal{A'}}^{\mathcal{A}}$ und $T_{\mathcal{B'}}^{\mathcal{B}}.$ Daraus folgt die Kommutativität des großen, äußeren Diagramms:

$\\ M_{\mathcal{B'}}^{\mathcal{A'}}(f) \circ T_{\mathcal{A'}}^{\mathcal{A}} \stackrel{(3)}{=} M_{\mathcal{B'}}^{\mathcal{A'}}(f) \circ \Phi_{\mathcal{A'}}^{-1} \circ \Phi_{\mathcal{A}} 
\stackrel{(2)}{=} \Phi_{\mathcal{B}}^{-1} \circ f \circ \Phi_{\mathcal{A}}
\stackrel{(1)}{=} \Phi_{\mathcal{B'}}^{-1} \circ \Phi_{\mathcal{B}} \circ M_{\mathcal{A}}^{\mathcal{B}}(f) \\
\stackrel{(4)}{=} T_{\mathcal{B'}}^{\mathcal{B}} \circ M_{\mathcal{B}}^{\mathcal{A}}(f)$
Da $T_{\mathcal{A'}}^{\mathcal{A}}$ invertierbar ist, folgt die Behauptung.


## Korollar

Sind $\mathcal{A}$ und $\mathcal{B}$ Basen eines endlich-dimensionalen Vektorraums und ist $f: V \rightarrow V$ ein Endomorphismus, so gilt:
$M_{\mathcal{B}}(f) = T_{\mathcal{B}}^{\mathcal{A}} \circ M_{\mathcal{A}}(f) \circ T_{\mathcal{A}}^{\mathcal{B}}.$


## Satz und Definition 7.3

Für jede Matrix $A \in K^{m \times n}$ gilt: Zeilenrang(A) = Spaltenrang(A). Diese Zahl heißt $\textbf{Rang von A}$ und wird mit Rg(A) (oder rk(A)) bezeichnet. $\\$

Beweis: $\\$
Wir fassen $A \in K^{m \times n}$ als lineare Abbildung $A: K^n \rightarrow K^m$ auf. Nach dem Korollar zu 6.6 gibt es Basen $\mathcal{A}$ in $K^n$ und $\mathcal{B}$ in $K^m$, sodass $M_{\mathcal{B}}^{\mathcal{A}}(A)$ die folgende Form hat: 
$\\ M_{\mathcal{B}}^{\mathcal{A}}(A) = \begin{pmatrix} I_r & 0 \\ 0 & 0 \end{pmatrix} =: B$ mit $r = dim_K(Im(A)). \\$
Für B gilt offensichtlich: (*) Zeilenrang(B) = r = Spaltenrang(B)
Nach ÜA 39 ist $A = M_{\mathcal{K}_m}^{\mathcal{K}_n}(A).$
Seien $T = T_{\mathcal{K}_n}^{\mathcal{A}}$ und $S = T_{\mathcal{B}}^{\mathcal{K}_m}$ die Transformationsmatrizen für Basiswechsel von $\mathcal{A}$ zu $\mathcal{K}_n$ bzw. von $\mathcal{K}_m$ zu $\mathcal{B}.$ Dann erhalten wir nach 7.2 ($\rightarrow$ Transformationsformel) folgendes kommutatives Diagramm:

$$\\ \xymatrix{
K^n \ar[rrrrrr]^{M_{\mathcal{K}_m}^{\mathcal{K}_n}(A)=A} \ar[dd]_{T=T_{\mathcal{K}_n}^{\mathcal{A}}} \ar[rrd]_{\Phi_{\mathcal{K}_n}} & & & & & & K^m \ar[lld]^{\Phi_{\mathcal{K}_m}} \ar[dd]^{S=T_{\mathcal{B}}^{\mathcal{K}_m}} \\
 & & K^n \ar[rr]^A & & K^m & & \\
K^n \ar[rrrrrr]^{M_{\mathcal{B}}^{\mathcal{A}}(A)=B} \ar[rru]^{\Phi_{\mathcal{A}}} & & & & & & K^m \ar[llu]_{\Phi_{\mathcal{B}}} } 
\\$$

Wegen der Kommutativität des Diagramms gitl dann: $B = S \cdot A \cdot T. \\$
Es genügt zu zeigen: $\\$
$(1)$ Spaltenrang($S \cdot A \cdot T$) = Spaltenrang(A) $\\$
$(2)$ Zeilenrang($S \cdot A \cdot T$) = Zeilenrang(A) $\\$

Zu (1): $\\$
T invertierbar $\Rightarrow$ T Isomorphismus $\Rightarrow dim_K(Im(A \cdot T)) = dim_K(Im(A)) \\$
S invertierbar $\Rightarrow$ S Isomorphismus $\Rightarrow dim_K(Im(S \cdot A \cdot T)) = dim_K(Im(A \cdot T)) \\$
Insgesamt folgt: Spaltenrang($S \cdot A \cdot T$) = $dim_K(Im(S \cdot A \cdot T)) = dim_K(Im(A \cdot T)) = dim_K(Im(A))$ = Spaltenrang(A)
$\\$

Zu (2): $\\$
Es gilt: $(S \cdot A \cdot T)^T = T^T \cdot A^T \cdot S^T.$ Nach 5.6 sind mit T und S auch $T^T$ und $S^T$ invertierbar und daher auch Isomorphismen. Daher folgt wie bei (1): $\\$
Spaltenrang($T^T \cdot A^T \cdot S^T$) = Spaltenrang($A^T$) $\\$
Spaltenrang($T^T \cdot A^T \cdot S^T$) = Spaltenrang($(S \cdot A \cdot T)^T$) = Zeilenrang($S \cdot A \cdot T$) $\\$
Spaltenrang($A^T$) = Zeilenrang(A) $\\$
Insgesamt folgt: Zeilenrang($S \cdot A \cdot T$) = Zeilenrang(A).


## Bemerkung


$A \xrightarrow{elementare~Zeilenumformungen} \tilde{A}$ (in Zeilenstufenform) 
$\\$
Nach 4.4 gilt ZR(A) = ZR($\tilde{A}$)
$\Rightarrow$ Zeilenrang(A) = Zeilenrang($\tilde{A}$) $\\$
$\xRightarrow{7.3}$ Rg(A) = Rg($\tilde{A}$) $\\$

$\tilde{A} \xrightarrow{Spaltenvertauschungen} \tilde{\tilde{A}}$ (in Zeilenstufenform mit Pivots in den ersten r Spalten) $\\$
Natürlich gilt: Spaltenrang($\tilde{A}$) = Spaltenrang($\tilde{\tilde{A}}$) $\\$
$\xRightarrow{7.3}$ Rg($\tilde{A}$) = Rg($\tilde{\tilde{A}}$) $\\$

Insgesamt folgt: Rg(A) = Rg($\tilde{\tilde{A}}$).


## Satz 7.4

Seien A ~ (m,n) und B ~ (n,r) zwei Matrizen. Dann gilt: $\\ Rg(A)+Rg(B)-n \leq Rg(A \cdot B) \leq min \{ Rg(A), Rg(B) \}. \\$

Beweis: $\\$
Sei $f: K^n \rightarrow K^m$ die durch A, $g: K^r \rightarrow K^n$ die durch B und $h: K^r \rightarrow K^m$ die durch $A \cdot B$ definierte lineare Abbildung.
$$\xymatrix{
K^r \ar[rdd]_g \ar[rr]^h & & K^m \\
 & & & \\
 & K^n \ar[ruu]_f & }$$
 
Dann gilt: $dim_K(Im(h)) = Rg(A \cdot B),~dim_K(Im(f)) = Rg(A),$ und $dim_K(Im(g)) = Rg(B).$
$Im(g) \subseteq K^n$ ist ein Untervektorraum. Durch Einschränkung von f auf Im(g) erhalten wir daher die lineare Abbildung $f^*: Im(g) \rightarrow K^m$ mit $f^*(x) = f(x)$ für $x \in Im(g).$ Für $f^*$ gilt: $\\$
$(a)~ Im(f^*) = f^*(Im(g)) = f(Im(g)) = f(g(K^r)) = Im(f \circ g) = Im(h) \\$
$(b)~ Ker(f^*) = \{ x \in Im(g) \mid f^*(x) = 0 \} = \{x \in Im(g) \mid f(x) = 0 \} = Im(g) \cap Ker(f) \\$

Dimensionsformel für $f^*:\\$
$\underbrace{dim_K(Im(f^*))}_{\stackrel{(a)}{=} Rg(A \cdot B)} + dim_K(Ker(f^*)) = \underbrace{dim_K(Im(g))}_{= Rg(B)}$
$\Rightarrow (*) Rg(A \cdot B) = Rg(B) - dim_K(Ker(f^*)) \\$

Aus $Rg(A \cdot B) \leq Rg(B)$ und 
$Im(h) = Im(f \circ g) = f(Im(g)) \subseteq Im(f) \Rightarrow Rg(A \cdot B) \leq Rg(A)$ folgt:
$Rg(A \cdot B) \leq min \{ Rg(A), Rg(B) \} \\$

(b) $\Rightarrow Ker(f^*) = Im(g) \cap Ker(f) \subseteq Ker(f) 
\Rightarrow dim_K(Ker(f^*)) \leq dim_K(Ker(f))
\Rightarrow Rg(A \cdot B) \geq Rg(B) - dim_K(Ker(f)) \\$

Dimensionsformel für f: $\\$
$dim_K(Ker(f)) + \underbrace{dim_K(Im(f))}_{= Rg(A)} = n
\Rightarrow Rg(A \cdot B) \geq Rg(B) + Rg(A) - n$


Sei $f:K^n \rightarrow K^m$ eine lineare Abbdildung.
Sei $\mathcal{A}$ eine Basis in $K^n$ und $\mathcal{B}$ eine Basis in $K^m.$
$\Rightarrow M_{\mathcal{B}}^{\mathcal{A}}(f) =: A$
Sei $\mathcal{A'}$ eine Basis in $K^n$ und $\mathcal{B'}$ eine Basis in $K^m.$
$\Rightarrow M_{\mathcal{B'}}^{\mathcal{A'}}(f) =: B$
Seien $T := T_{\mathcal{A'}}^{\mathcal{A}}$ und $S := T_{\mathcal{B'}}^{\mathcal{B}}$ die entsprechenden Transformationsmatrizen, so gilt nach 7.2 
($\rightarrow$ Transformationsformel): $B = S \cdot A \cdot T^{-1}.$

Einen solchen Zusammenhang zwischen zwei beliebigen Matrizen A,B ~ (m,n) gibt es nicht, wenn A und B nicht darstellende Matrizen derselben Abbildung f sind. Entsprechend gilt für A,B ~ (n,n): Genau dann gibt es eine invertierbare Matrix S ~ (n,n), sodas $B = S \cdot A \cdot S^{-1}$ gilt, wenn A und B die darstellenden Matrizen desselben Endomorphismus $f: K^n \rightarrow K^n$ bzgl. verschiedener Basen $\mathcal{A}$ und $\mathcal{B}$ in $K^n$ sind.


## Definition 7.5

$(1)$ Zwei Matrizen $A,B \in K^{m \times n}$ heißen $\textbf{äquivalent},$ wenn es invertierbare Matrizen $S \in K^{m \times m}$ und $T \in K^{n \times n}$ gibt, sodass $B = S \cdot A \cdot T^{-1}. \\$
$(2)$ Zwei quadratische Matrizen $A,B \in K^{n \times n}$ heißen 
$\textbf{ähnlich},$ wenn es eine invertierbare Matrix $S \in K^{n \times n}$ gibt, sodass $B = S \cdot A \cdot S^{-1}. \\$


## Einschub: Begriff der Äquivalenzrelation

## Definition 7.6

$(1)$ Sei M eine nichtleere Menge. Dann heißt eine nichtleere Teilmenge $R \subseteq M \times M$ eine $\textbf{Relation}$ auf M. Ist $(x,y) \in R,$ so schreibt man xRy und sagt "x ist in Relation zu y". $\\$

$(2)$ Eine Relation ~ auf einer nichtleeren Menge M heißt 
$\textbf{Äquivalenzrelation}$ auf M, wenn folgende Axiome gelten: $\\$
$(Ä1)$ Reflexivität: $x \sim x \forall x \in M \\$
$(Ä2)$ Symmetrie: $x \sim y \Rightarrow y \sim x \forall x,y \in M \\$
$(Ä3)$ Transitivität: $x \sim y$ und $y \sim z \Rightarrow x \sim z \forall x,y,z \in M \\$

$(3)$ Ist ~ eine Äquivalenzrelation auf einer nichtleeren Menge M, so heißt eine Teilmenge $A \subseteq M$ eine $\textbf{Äquivalenzklasse}$ (bzgl. ~), wenn gilt: $\\$
$(i) A \neq \emptyset \\$
$(ii) x,y \in A \Rightarrow x \sim y \\$
$(iii) x \in A, y \in M, x \sim y \Rightarrow y \in A \\$


## Beispiel

Die Äquivalenz von Matrizen ist eine Äquivalenzrelation auf $K^{m \times n}. \\$
Die Ähnlichkeit von Matrizen ist eine Äquivalenzrelation auf $K^{n \times n}.$


## Satz 7.7

Eine Äquivalenzrelation ~ auf einer nichtleeren Menge M bewirkt eine Einteilung von M in paarweise disjunkte Äquivalenzklassen.


Beweis:

Sei $a \in M.$ Dann sezten wir $A := \{ x \in M \mid x \sim a \}. \\$
Wir zeigen: A ist eine Äquivalenzrelation und enthält a. $\\$
Wegen a ~ a (nach (Ä1)) ist $a \in A.$ Insbesondere ist daher $A \neq \emptyset.$ 
Seien $x,y \in A,$ d.h. x ~ a und y ~ a. $\xRightarrow{(Ä2)}$ x ~ a und a ~ y 
$\xRightarrow{(Ä3)}$ x ~ y. $\\$
Sei $x \in A, y \in M$ und x ~ y, d.h. x ~ a und $y \in M$ und x ~ y. 
$\xRightarrow{(Ä2)}$ y ~ x und x ~ a $\xRightarrow{(Ä3)}$ y ~ a $\Rightarrow y \in A.$
Damit sind (i),(ii) und (iii) von 7.6 (3) gezeigt. Also ist A eine Äquivalenzklasse mit $a \in A.$ Damit gilt: Jedes $a \in M$ liegt in mindestens einer Äquivalenzklasse.
Wir zeigen: Sind A,A' zwei Äquivalenzklassen, so gilt A = A' oder $A \cap A' = \emptyset.$ Wir müssen also zeigen: Ist $A \cap A' \neq \emptyset,$ so ist A = A'.
Sei $a \in A \cap A',$ d.h. $a \in A$ und $a \in A'.$
Sei $x \in A.$ Dann gilt x ~ a, da $a \in A.$ Da $a \in A',$ folgt $x \in A',$ d.h. $A \subseteq A'.$ Analog folgt $A' \subseteq A.$ 
Insgesamt folgt A = A'. $\\$
Die Äquivalenzklassen sind also paarweise disjunkt und jedes Element aus M liegt in genau einer Äquivalenzklasse.


Eine Idee, die mit der Definition einer Äquivalenzrelation verbunden ist, ist es, in die Menge M unter einem bestimmten Gesichtspunkt (der durch die Äquivalenzrelation ausgedrückt ist) eine gewisse Ordnung zu bringen. Die Menge M wird übersichtlicher, indem man zur Menge der Äquivalenzklassen übergeht. Man denke etwa an eine Bücherei, in der jeweils die Bücher, die dasselbe Fachgebiet behandeln, zusammen aufgestellt werden.Jedes Element a einer Äquivalenzklasse A nennt man einen Repräsentanten der Äquivalenzklasse. Eine vollständige Übersicht über die Menge M erhält man, wenn man sämtliche Äquivalenzklassen durch die Wahl jeweils eines besonders einfachen (typischen) Repräsentanten in jeder Äquivalenzklasse kennzeichnen kann. Ein Beispiel, wo dies möglich ist, stellt der Begriff der Äquivalenz von Matrizen dar. Hier können wir leicht die Äquivalenzklassen durch den Rang der zu ihnen gehörenden Matrizen charakterisieren und jeweils eine Matrix von besonders einfachen Aussehen als Repräsentant (”Normalform”) auszeichnen. Viel schwieriger ist die Behandlung dieses Problems im Falle des Begriffs der Ähnlichkeit.


## Lemma und Definition 7.8

Zwei Matrizen vom gleichen Typ (m,n) sind genau dann äquivalent, wenn sie denselben Rang haben. Insbesondere ist jede (m,n)-Matrix vom Rang r äquivalent zu $\begin{pmatrix} I_r & 0\\ 0 & 0 \end{pmatrix}$ ~ (m,n). Diese Matrizen repräsentieren die Äquivalenzklassen und heißen $\textbf{Normalform}. \\$

Beweis: $\\$
Sei $A \in K^{m \times n}$ und Rg(A) = r. Nach dem Korollar zu 6.6 gibt es Basen $\mathcal{A}$ in $K^n$ und $\mathcal{B}$ in $K^m,$ sodass 
$M_{\mathcal{B}}^{\mathcal{A}}(A) = \begin{pmatrix} I_r & 0 \\ 0 & 0 \end{pmatrix}.$ Seien $T = T_{\mathcal{A}}^{\mathcal{K}_n}$ und $S = T_{\mathcal{B}}^{\mathcal{K}_m}$ Transformationsmatrizen. Dann gilt nach der Transformationsformel $M_{\mathcal{B}}^{\mathcal{A}}(A) = S \cdot A \cdot 
T^{-1}.$ Also gilt $S \cdot A \cdot T^{-1} = \begin{pmatrix} I_r & 0 \\ 0 & 0 \end{pmatrix},$ d.h. A ist äquivalent zu $\begin{pmatrix} I_r & 0 \\ 0 & 0 \end{pmatrix}.$
Sind A und B Matrizen mir Rg(A) = r und Rg(B) = r, so sind A und B beide äquivalent zu $\begin{pmatrix} I_r & 0 \\ 0 & 0 \end{pmatrix}.$
Wegen der Transitivität sind A und B äquivalent zueinander.

Umgekehrt - Äquivalenz zu B: $\\$
$\xRightarrow{7.5}$ Es existieren invertierbare Matrizen S und T, sodass $B = S \cdot A \cdot T^{-1}.$ Da S und T Isomorphismen darstellen, gilt dann:
$Rg(A) = dim_K(Im(A)) = dim_K(Im(S \cdot A \cdot T^{-1})) = dim_K(Im(B)) = 
Rg(B).$


## Lemma 7.9

Sei A ~ (m,n) eine Matrix. Dann gilt: $\\$
$(1) Ker(A^T \cdot A) = Ker(A)$ und $Ker(A \cdot A^T) = Ker(A^T) \\$
$(2) Rg(A^T \cdot A) = Rg(A)$ und $Rg(A \cdot A^T) = Rg(A^T) = Rg(A) \\$

Beweis: $\\$

$(1)$ ÜA 13 $\\$
$(2) Rg(A^T \cdot A) = dim_K(Im(A^T \cdot A))
= n - dim_K(Ker(A^T \cdot A))
= n - dim_K(Ker(A))
= dim_K(Im(A))
= Rg(A)$
Analog: $Rg(A \cdot A^T) = Rg(A^T).$
Es gilt immer: $Rg(A) = Rg(A^T).$