#6. Lineare Abbildungen und Matrizen

##Erinnerung
- Begriff der linearen Abbildung $f: V \to W$ und die Begriffe Isomorphismus, Endomorphismus, Automorphismus
- Bisher bewiesene Eigenschaften: Satz 1.11 und Folgerungen daraus, $f(V)=Imf \subseteq W$ und $f^{-1}(\{0\})=Kerf \subseteq V$ sind  UVR, $f$ surjektiv $\iff Imf =W, f$ injektiv $\iff Kerf=\{0\}$

##Lemma 6.1
Ist $f: V \to W$ eine injektive lineare Abbildung, so gilt: $v_1, ..., v_n \in V$ linear unabhängig $\implies f(v_1),...,f(v_n) \in W$ linear unabhängig.

##Beweis
$\alpha_1 \cdot f(v_1)+...+\alpha_n \cdot f(v_n) = 0 \\$
$\implies f(\alpha_1 \cdot v_1+ ... +\alpha_n \cdot v_n) = 0$, da $f$ linear $\\
\implies \alpha_1 \cdot v_1+ ... + \alpha_n \cdot v_n = 0$, da $f$ injektiv $\\
\implies \alpha_1 = 0, ..., \alpha_n =0$, da $v_1,...,v_n$ linear unabhängig.

##Satz 6.2
Sei $f: V \to W$ eine lineare Abbildung und $dimV$ endlich. Sind Basen $(v_1,...,v_k)$ von $Kerf$ und $(w_1,...,w_r)$ von $Imf$ sowie beliebige Vektoren $u_1,...,u_r$ mit $f(u_i)=w_i$ für $i=1,...,r$ (also Urbilder der Basisvektoren von $Imf$ gegeben, so ist $\mathcal{A} = (u_1,...,u_r, v_1,..., v_k)$ eine Basis von V. Insbesondere folgt daraus die Dimensionsformel: $$ dimV = dim(Kerf)+dim(Imf) $$

##Beweis
(1) $\mathcal{A}$ ist ein Erzeugendensystem von $V: \\$
Sei $v\in V$ beliebig. Dann ist $f(v) \in Imf$. da $w_1,...,w_r$ Basis von $Imf$, folgt: Es existieren $\alpha_1,...,\alpha_r \in K$ mit $f(v)= \alpha_1 \cdot w_1 + ... + \alpha_r \cdot w_r$. Mit diesen Skalaren setze $v':=\alpha_1 \cdot u_1 + ... + \alpha_r \cdot u_r$. Dann gilt: $\\$
$f(v')=f(\alpha_1 \cdot u_1+...+\alpha_r \cdot u_r) \\
= \alpha_1 \cdot f(u_1)+...+\alpha_r \cdot f(u_r) \\
= \alpha_1 \cdot w_1+...+\alpha_r \cdot w_r \\
= f(v) \\$
Daraus folgt: $f(v-v') = 0$, d.h. $v-v' \in Kerf \\$
Da $v_1,...,v_k$ Basis von $Kerf$, folgt: Es existieren $\beta_1,...,\beta_k \in K$ mit $v-v'=\beta_1 \cdot v_1+...+ \beta_k \cdot v_k \\$
Insgesamt folgt: $v=\alpha_1 \cdot u_1+...+\alpha_r \cdot u_r+\beta_1 \cdot v_1+...+\beta_k \cdot v_k, v \in span(\mathcal{A}). \\$
(2) $\mathcal{A}$ ist linear unabhängig: $\\$
$\circledast \mu_1 \cdot u_1+...+\mu_r \cdot u_r+\lambda_1 \cdot v_1+...+\lambda_k \cdot v_k = 0 \\
\implies f(\mu_1 \cdot u_1+...+\mu_r \cdot u_r+\lambda_1 \cdot v_1+...+\lambda_k \cdot v_k) = f(0)=0 \\
\implies \mu_1 \cdot f(u_1)+...+\mu_r \cdot f(u_r)+\lambda_1 \cdot f(v_1)+...+\lambda \cdot f(v_k)=0 \\
\implies \mu_1 \cdot w_1 +...+\mu_r \cdot w_1 =0$, da $f(v_i)=0 \\
\implies \mu_1=,...,\mu_r=0$, da $w_1,...w_r$ linear unabhängig. $\\$
Also gilt wegen $\circledast: \lambda_1 \cdot v_1+...+\lambda_k \cdot v_k=0 \\
\implies \lambda_1=0,...,\lambda_k=0$, da $v_1,...,v_k$ linear unabhängig $\\$
(3) Dimensionformel: $\\$
$\mathcal{A}=(u_1,...,u_r,v_1,...,v_k)$ Basis von V mit $r=dim(Imf)$ und $k=dim(Kerf) \\
\implies dimV=r+k$

##Korollar
Seien $V,W$ endlich-dimensionale VR, $dimV=dimW$ und $f:V \to W$ eine lineare Abbildung. Dann sind folgende Aussagen äquivalent:

(1) $f$ ist injektiv
(2) $f$ ist surjektiv
(3) $f$ ist Isomorphismus

##Satz 6.3
Seien $V,W$ VR, $v_1,...,v_r \in V$ und $w_1,...,w_r \in W$. Dann gilt:

(1) $v_1,...,v_r$ linear unabhängig $\implies$ es gibt mindestens eine lineare Abbildung $f:V \to W$ mit $f(v_i)=w_i$ für $i=1,...,r$
(2) $v_1,...,v_r$ Basis von $V \implies$ es gibt genau eine lineare Abbildung $f:V \to W$ mit $f(v_i)=w_i$ für $i=1,...,r.$
Dabei hat diese lineare Abbildung folgende Eigenschaften:
(a) $Imf=span(w_1,...,w_r)$
(b) $f$ injektiv $\iff w_1,...,w_r$ linear unabhängig

##Beweis
(2) Sei $(v_1,...,v_r)$ eine Basis von $V$. Seie $v \in V$ beliebig. $\\
\implies v= \alpha_1 \cdot v_1+...+ \alpha_1 \cdot v_r \\$
Da $f(v_i)=w_i$ für $i=1,...,r$ und $f$ linear sein soll, gilt: $\\
f(v)=f(\alpha_1 \cdot v_1+...+\alpha_r \cdot v_r) \\
=\alpha_1 \cdot f(v_1)+...+\alpha_r \cdot f(v_r) \\
= \alpha_1 \cdot w_1+...+\alpha_r \cdot w_r \\$
Es gibt also höchstens eine solche Abbildung, nämlich gerade bestimmte. $\\$
Mindestens eine lineare Abbildung? $\\$
(L1)$f(v+v')=f(\alpha_1 \cdot v_1+...+\alpha_r \cdot v_r+\alpha'_1 \cdot v_1+...+\alpha'_r \cdot v_r) \\
=f((\alpha_1+\alpha'_1) \cdot v_1+...+(\alpha_r+\alpha'_r) \cdot v_r) \\
=(\alpha+\alpha'_1) \cdot w_1+...+(\alpha_r+\alpha'_r) \cdot w_r \\
=\alpha_1 \cdot w_1+...+\alpha_r \cdot w_r+\alpha'_1 \cdot w_1+...+\alpha'_r \cdot w_r \\
=f(v) + f(v') \\$
(L2) $f(\alpha \cdot v)=f(\alpha \cdot \alpha_1 \cdot v_1+...+\alpha \cdot\alpha_r \cdot v_r) \\
=\alpha \cdot \alpha_1 \cdot w_1+...+\alpha \cdot \alpha_r \cdot w_r \\
=\alpha \cdot (\alpha_1 \cdot w_1+...+ \alpha_r \cdot w_r \\
=\alpha \cdot f(v) \\$
Nachzuweisen sind noch (a) und (b): $\\$
(a) $v \in V \implies f(v)=f(\alpha_1 \cdot v_1+...+\alpha_r \cdot v_r)= \alpha_1 \cdot w_1+...+\alpha_r \cdot w_r \in span(w_1,...,w_r) \\$
Also gilt: $Imf \subseteq span(w_1,...,w_r) \\
w\in span(w_1,...,w_r) \implies w=\lambda_1 \cdot w_1+...+\lambda_r \cdot w_r \\
\implies w= f(\lambda_1 \cdot v_1+...+\lambda_r \cdot v_r) \in Imf \\$
Also gilt: $span(w_1,...,w_r) \subseteq Imf \\$
(b) $"\Rightarrow:$ Lemma 6.1 $\\
"\Leftarrow":$ Sei $v=\alpha_1 \cdot v_1+...+\alpha_r \cdot v_r \in V$ und $f(v)=0 \\
\implies \alpha_1 \cdot w_1 +...+\alpha_r \cdot w_r=f(v)=0 \implies \alpha_1 =0,..., \alpha_r =0$, da $w_1,...,w_r$ linear unabhängig $\implies v=0 \implies Kerf={0} \\$
(1) $v_1,...,v_r$ linear unabhängig $\overset{3.14}{\implies} v_1,..,v_r$ kann ergänzt werden zu einer Basis $(v_1,...,v_r,v_{r+1},...,v_n)$ von $V. \\$
Wählen wir nun beliebig zu $w_1,...,w_r$ weitere Vektoren $w_{r+1},...,w_r$, so können wir nach (2) genau eine lineare Abbildung $f:V \to W$ angeben, für die $f(v_i)=w_i, i=1,...,r,r+1,...,n$, gilt.

###Bemerkung
$n-r$ ist ein Maß dafür, wie weit $f$ davon entfernt ist, eindeutig zu sein.

##Korollar A
Sind $V$ und $W$ endlich-dimensionale VR, so gilt: $\\$
Es gibt einen Isormorphismus $f:V\to W$ genaz dann, wenn $dimV=dimW$.

##Beweis
$"\Rightarrow": f:V \to W$ Isomorphismus $\implies dim(Kerf)=0$ und $dim(Imf)=dimW \overset{6.2}{\implies} dimv=dimW \\
"\Leftarrow": dimV=dimW \implies V$ und $W$ haben Basen gleicher Länge $n$, etwa $\mathcal{A}=(v_1,...,v_n)$ Basis von $V$ und $\mathcal{B}=(w_1,...,w_n)$ Basis von $W$. Nach 6.3 gibt es daher (genau) einen Isomorphismus $f:V \to W$ mit $f(v_i)=w_i, i=1,...,n.$

##Korollar B
Sei $V$ ein VR und $dimV=n$. Dann gibt es zu jeder Wahl einer Basis $\mathcal{B}=(v_1,...,v_n)$ von $V$ genau einen Isomorphismus $\Phi_\mathcal{B} : K^n \to V$  mit $\Phi_\mathcal{B} (e_i)=v_i$ für $i=1,...,n. \\$
Bezüglich der Basis $\mathcal{B}(v_1,..,v_n)$ ist jeder Vektor $v \in V$ eindeutig gegeben durch seine Darstellung $v=x_1 \cdot v_1+...+x_n \cdot v_n. \\$
Definitionsgemäß gilt dann für $x= \begin{pmatrix} x_1 \\ \vdots \\ x_n \end{pmatrix} \in K^n: \\
\Phi_\mathcal{B} (x)= \Phi_\mathcal{B}(x_1 \cdot e_1+...+x_n \cdot e_n)=x_1 \cdot v_1+...+x_n \cdot v_n = v \\$
Das bedeutet: Unter dem Isomorphismus $\Phi_\mathcal{B}$ entspricht der Vektor $v =x_1 \cdot v_1+...+x_n \cdot v_n \in V$ dem Vektor $\Phi_\mathcal{B}^{-1}(v)=x= \begin{pmatrix} x_1 \\ \vdots \\ x_n \end{pmatrix} \in K^n$.

##Definition 6.4
Sei $V$ ein KVR und $dimV=n$. Dann heißt der zu einer Basis $\mathcal{B}=(v_1,...,v_n)$ von $V$ eindeutig bestimmte Isomorphismus $\Phi_\mathcal{B} : K^n \to V$ mit $\Phi_\mathcal{B} (e_i) =v_i$ für $i=1,...,n$ das durch $\mathcal{B}$ bestimmte Koordinatensystem in $V$. Für $v=x_1 \cdot v_1+...+x_n \cdot v_n \in V$ heißt $x= \begin{pmatrix} x_1 \\ \vdots \\ x_n \end{pmatrix} = \Phi_\mathcal{B}^{-1} (v)$ die Koordinatendarstellung von $v$ bzgl. $\mathcal{B}$ und $x_1,...,x_n$ heißten die Koordinaten von $v. \\$
(Zur Berechnung: $(v_1,...,v_n) \cdot
\begin{pmatrix}
  x_1 \\
  \vdots
  \\ x_n
\end{pmatrix}
= v)$

##Lemma 6.5
Zu jeder linearen Abbildung $f: K^n \to K^m$ gibt es genau eine Matrix $A \sim (m,n)$ sodass $f(x)=A \cdot x$ für alle $x \in K^n$.

##Beweis
Sei $(e_1,...,e_n)$ die Standardbasis von $K^n$ und sei $f(e_1)= \begin{pmatrix}
  a_{11} \\
  \vdots \\
  a_{m1}
\end{pmatrix}
,..., f(e_n) =
\begin{pmatrix}
  a_{1n} \\
  \vdots \\
  a_{mn}
\end{pmatrix}
.$ Dann ist $A=
\begin{pmatrix}
  a_{11} & \cdots & a_{1n} \\
  \vdots & & \vdots \\
  a_{m1} & \cdots & a_{mn}
\end{pmatrix}$
, da $A \cdot x = x_1 \cdot
\begin{pmatrix}
  a_{11} \\
  \vdots \\
  a_{m1}
\end{pmatrix}
+ ... + x_n \cdot
\begin{pmatrix}
  a_{1n} \\
  \vdots \\
  a_{mn}
\end{pmatrix}
= x_1 \cdot f(e_1)+...+x_n \cdot f(e_n) = f(x)$

##Satz 6.6
Seien $V$ und $W$ KVR, $\mathcal{A}=(v_1,...,v_n)$ Basis von $V$ und $\mathcal{B}=(w_1,...,w_m)$ Basis von $W$. Dann gibt es zu jeder linearen Abbildung $f: V \to W$ gneau eine Matrix $A=(a_{ij}) \in K^{(m,n)}$, sodass $f(v_j)= \sum\limits_{i=1}^m  a_{ij} \cdot w_i$ für $j=1,...,n. \\$
Die Matrix, die $f$ bzgl. der Basen $\mathcal{A}$ und $\mathcal{B}$ darstellt, bezeichnet man mit $M_{\mathcal{B}}^{\mathcal{A}} (f)$ und nennt sie dia darstellende Matrix von $f$ bzgl. $\mathcal{A}$ und $\mathcal{B}$.

##Beweis
Da $\mathcal{B}$ Basis, ist zu jedem $f(v_j)= \sum\limits_{i=1}^m  a_{ij} \cdot w_i$ die Linearkombination eindeutig bestimmt und damit die $j$-te Spalte von $A$. Folglich ist $M_{\mathcal{B}}^{\mathcal{A}} (f)$ eindeutig bestimmt.

##Folgerung
Seien $V,W$ KVR, $dimV=n, dimW=m, \mathcal{A}=(v_1,...,v_n)$ eine Basis von $V, \mathcal{B}=(w_1,...,w_m)$ eine Basis von $W, \Phi_\mathcal{B} (e_j^{(n)})=v_j$ und $\Phi_\mathcal{B} : K^m \to W$ mit $\Phi_\mathcal{B} (e_i^{(m)} = w_i$ seien die durch die Basen $\mathcal{A}$ und $\mathcal{B}$ bestimmten Koordinatensysteme in $V$ bzw. $W$. Dann erhält man für jede lineare Abbildung $f:V \to W$ das folgende Diagramm:

$$\xymatrix{ K^n \ar[d]_{M^{\mathcal{A}}_{\mathcal{B}}(f)} \ar[r]^{\Phi_{\mathcal{A}}} & V \ar[d]^f \\
              K^m \ar[r]^{\Phi_{\mathcal{B}}} & W } $$

wobei $\Phi_{\mathcal{B}} \circ M^{\mathcal{A}}_{\mathcal{B}} (f) = f \circ \Phi_{\mathcal{A}}. \\$
Oder gleichbedeutend: $M^{\mathcal{A}}_{\mathcal{B}} (f) = \Phi^{-1}_{\mathcal{B}} \circ f \circ \Phi_{\mathcal{A}} \\$
Man sagt kurz: Das Diagramm ist kommutativ.

##Beweis
Nach Satz 6.3 genügt es zu zeigen, dass $\Phi_{\mathcal{B}} \circ M^{\mathcal{A}}_{\mathcal{B}} (f)$ und $f \circ \Phi_{\mathcal{A}}$ auf der kanonischen Basis $(e_1^{(n)},...,e_n^{(n)})$ von $K^n$ übereinstimmen. Setze $M^{\mathcal{A}}_{\mathcal{B}} (f) =: A. \\
\left.
\begin{aligned}
\Phi_{\mathcal{B}} (A(e_j^{(n)})) = \Phi_{\mathcal{B}} (A_{\bullet j}) = \sum\limits_{i=1}^n  a_{ij} \cdot w_i \\
f(\Phi_{\mathcal{A}} (e_j^{(n)})) = f(v_j) \overset{6.6}{=} \sum\limits_{i=1}^n  a_{ij} \cdot w_i
\end{aligned}
\right\} \implies Gleichheit$

###Bemerkung
Ist$W=V$, als $f:V \to V$ ein Endomorphismus, so wählt man im Allgemeinen $\mathcal{A} = \mathcal{B}. \\$
Bezeichnung: $M_{\mathcal{A}} (f)$ statt $M_{\mathcal{A}}^{\mathcal{A}} (f). \\$
Die Matrix der identischen Abbildung $id_V : V \to V$ mit $id_V(v)=v$ bzgl. einer Basis $\mathcal{A}$ in $V$ ist $M_{\mathcal{A}} (id_V) = I_n.$

###Beispiel
$\mathcal{A} = (v_1,v_2,v_3)$ sei eine Basis von $\mathbb{R}^3 \\
\mathcal{B} = (w_1,w_2)$ sei eine Basis von $\mathbb{R}^2\\$
lineare Abbildung $f: \mathbb{R}^3 \to \mathbb{R}^2$ mit $f(v_1)=2 \cdot w_1+w_2, f(v_2)=w_1 - w_2 , f(v_3)=w_1 - 2 \cdot w_2 \\
M_{\mathcal{B}}^{\mathcal{A}} (f) =
\begin{pmatrix}
2 & 1 & 1 \\
1 & -1 & -2
\end{pmatrix} \\
\Phi_{\mathcal{A}} : \mathbb{R}^3 \to \mathbb{R}^3$ mit $\Phi_{\mathcal{A}} (e_i) = v_i \\
\begin{pmatrix}
  \alpha_1 \\
  \alpha_2 \\
  \alpha_3
\end{pmatrix}
\overset{\Phi_{\mathcal{A}}}{\mapsto} \alpha_1 \cdot v_1 + \alpha_2 \cdot v_2 + \alpha_3 \cdot v_3 \\
\Phi_{\mathcal{B}} : \mathbb{R}^2 \to \mathbb{R}^2$ mit $\Phi_{\mathcal{B}} (e_j) = w_j \\
\begin{pmatrix}
\beta_1 \\ \beta_2
\end{pmatrix}
\overset{\Phi_{\mathcal{B}}}{\mapsto} \beta_1 \cdot w_1 + \beta_2 \cdot w_2 \\$
Nach der Folgerung gilt dann: $\Phi_{\mathcal{B}} (M_{\mathcal{B}}^{\mathcal{A}} (f) \cdot
\begin{pmatrix}
  \alpha_1 \\
  \alpha_2 \\
  \alpha_3
\end{pmatrix}
) = f(\Phi_{\mathcal{A}} \cdot
\begin{pmatrix}
  \alpha_1 \\
  \alpha_2 \\
  \alpha_3
\end{pmatrix}
) \\$
Sei $v = -2 \cdot v_1 + 6 \cdot v_2 -5 \cdot v_3.$ Bestimme $f(v): \\
f(v) = f(-2 \cdot v_1 + 6 \cdot v_2 - 5 \cdot v_3) \\
= f( \Phi_{\mathcal{A}} \cdot
\begin{pmatrix}
  -2 \\
  6 \\
  -5
\end{pmatrix} \\
= \Phi_{\mathcal{B}} (M_{\mathcal{B}}^{\mathcal{A}} (f) \cdot
\begin{pmatrix}
  -2 \\
  6 \\
  -5
\end{pmatrix} ) \\
= \Phi_{\mathcal{B}} (
\begin{pmatrix}
2 & 1 & 1 \\
1 & -1 & -2
\end{pmatrix}
\cdot
\begin{pmatrix}
  -2 \\
  6 \\
  -5
  \end{pmatrix}
  ) \\
= \Phi_{\mathcal{B}}
\begin{pmatrix}
  -3 \\
  2
\end{pmatrix} \\
= -3 \cdot w_1 + 2 \cdot w_2$

##Korollar (zu Satz 6.6)
Sei $f: V \to W$ linear, $dimV=n, dimW=m$ und $dim(Imf)=r$. Dann gibt es Basen $\mathcal{A}$ (von $V$) und $\mathcal{B}$ (von $W$), sodass gilt. $\\$
$$M_{\mathcal{B}}^{\mathcal{A}} (f) =
\begin{pmatrix}
  I_r & 0 \\
  0 & 0
\end{pmatrix}
\sim (m,n)$$

##Beweis
Nach Satz 6.2 gibt es eine Basis $\mathcal{A}=(u_1,...,u_r,v_1,...,v_{n-r})$ von $V$ mit $(v_1,...,v_{n-r})$ ist eine Basis von $Kerf$ und $(w_1=f(u_1),...,w_r=f(u_r))$ ist eine Basis von $Imf.$ Wir ergänzen $(w_1,...,w_r)$ zu einer Basis von $\mathcal{B} = (w_1,...,w_r, w_{r+1},...,w_m)$ von $W$ (mit dem Basisergänzungssatz). Dann gilt: $\\
\left.
\begin{aligned}
f(u_j) = w_j \text{ für } j=1,...,r \\
f(v_j) = 0 \text{ für } j=1,...,n-r
\end{aligned}
\right \} \implies
M_{\mathcal{B}}^{\mathcal{A}} (f) = \begin{pmatrix} I_r & 0 \\ 0 & 0 \end{pmatrix}$

##Satz 6.7
Seien $U,V,W$ KVR mit Basen $\mathcal{A}, \mathcal{B}, \mathcal{C}$ und seien $g: U \to V, f: V \to W$ lineare Abbildungen. Dann gilt $M^{\mathcal{A}}_{\mathcal{C}} (f \circ g) = M^{\mathcal{B}}_{\mathcal{C}} (f) \cdot M^{\mathcal{A}}_{\mathcal{B}} (g)$

##Beweis (Hier fehlen noch die Zahlen und die Klammer im DIagramm)
\xymatrix{
K^r \ar[rrr]^{\Phi_{\mathcal{A}}} \ar[dr]^{M^{\mathcal{A}}_{\mathcal{B}}(g)} \ar[dd]_{M^{\mathcal{A}}_{\mathcal{C}}(g \circ f)} & & &  U \ar[dd]^{g \circ f} \ar[dl]^g \\
  &  K^m \ar[r]^{\Phi_{\mathcal{B}}} \ar[dl]^{M^{\mathcal{B}}_{\mathcal{C}}(f)}  & V \ar[dr]^f & \\
K^n \ar[rrr]^{\Phi_{\mathcal{C}}} &   &   &   W}

Zz: Das Diagramm $\textcircled{5}$ ist kommutativ $\\$
Die Diagramme $\textcircled{1}, \textcircled{2}$ und $\textcircled{3}$ sind kommutativ nach Definition der darstellenden Matrizen. $\\$
Das Diagramm $\textcircled{4}$ ist natürlich kommutativ. $\\$
Damit folgt: $\Phi_{\mathcal{C}} \circ M^{\mathcal{B}}_{\mathcal{C}}(f) \circ M^{\mathcal{A}}_{\mathcal{B}}(g) \\
\overset{2}{=} f \circ \Phi_{\mathcal{B}} \circ M^{\mathcal{A}}_{\mathcal{B}}(g) \\
\overset{1}{=} f \circ g \circ \Phi_{\mathcal{A}} \\
\overset{3}{=} \Phi_{\mathcal{C}} \circ M^{\mathcal{A}}_{\mathcal{C}} (f \circ g) \\$
Da $\Phi_{\mathcal{C}}$ Isomorphismus folgt: $M^{\mathcal{B}}_{\mathcal{C}}(f) \cdot M^{\mathcal{A}}_{\mathcal{B}}(g) = M^{\mathcal{A}}_{\mathcal{C}}(f \circ g)$

##Folgerung
Sei $V$ ein KVR mit der Basis $\mathcal{B}$ und seien $f,g: V \to V$ Endomorphismen. Dann gilt  $\\M^{\mathcal{B}}(f \circ g) = M_{\mathcal{B}}(f) \cdot M_{\mathcal{B}}(g).$
