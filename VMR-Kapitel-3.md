# Kapitel 3: Basis und Dimension eines Vektorraums


## Definition 3.1

Sei V ein K-Vektorraum und $v_1, \ \dotso \ , \ v_r \in V.$ Ein Vektor $v \in V$ heißt eine $\textbf{Linearkombination}$ von $v_1, \ \dotso \ , \ v_r,$ wenn es Skalare $\alpha_1, \ \dotso \ , \ \alpha_r \in K$ gibt, sodass $v = \alpha_1 \cdot v_1 + \dotso + \alpha_r \cdot v_r = \sum\limits_{i=1}^r \alpha_i \cdot v_i.$


## Bezeichnungen

Sei V ein K-Vektorraum und I eine nichtleere Menge, die wir als Indexmenge benutzen. Zu jedem $i \in I$ sei ein Vektor $v_i \in V$ gewählt. Die Menge dieser $v_i \in V, \ i \in I,$ heißt eine $\textbf{Familie}$ von Vektoren aus V und wird mit $(v_i)_{i \in I}$ bezeichnet. Für eine solche Familie $(v_i)_{i \in I}$ bilden wir die Menge aller möglichen Linearkombinationen von endlich vielen Vektoren der Familie und bezeichnen sie mit $$span((v_i)_{i \in I}) = \{ v \in V: \exists \ r \in \mathbb{N}, i_1, \dotso, i_r \in I, \alpha_1, \ \dotso \ , \ \alpha_r \in K: v = \sum\limits_{i=1}^r \alpha_i \cdot v_i \}$$


## Satz und Definition 3.2

Sei V ein K-Vektorraum, I eine nichtleere Menge und $(v_i)_{i \in I}$ eine Familie von Vektoren aus V. Dann gilt: $\\$
(1) $span((v_i)_{i \in I})$ ist ein Untervektorraum von V. Er heißt der von der Familie $(v_i)_{i \in I}$ aufgespannte Vektorraum. $\\$
(2) Ist $U \subseteq V$ ein Untervektorraum von V und $v_i \in U$ für alle $i \in I,$ so ist $span((v_i)_{i \in I}) \subseteq U$ ein Untervektorraum von U.
$\\$

Beweis:

(1) Nachweis von (UV1) - (UV3) aus 1.5: $\\$
(UV1) $v_j \in span((v_i)_{i \in I})$ für jedes $j \in I \ \Rightarrow span((v_i)_{i \in I}) \neq \emptyset. \\$
(UV2) $u, v \in span((v_i)_{i \in I}) \Rightarrow u = \alpha_1 \cdot v_{i_1} + \dotso + \alpha_r \cdot v_{i_r}$ und $v = \beta_1 \cdot v_{j_1} + \cdot + \beta_s \cdot v_{j_s} \\$
(UV3) $\alpha \in K, \ u \in span((v_i)_{i \in I}) \Rightarrow u = \alpha_1 \cdot v_{i_1} + \dotso + \alpha_r \cdot v_{i_r} \Rightarrow \alpha \cdot u = (\alpha \cdot \alpha_1) \cdot v_{i_1} + \dotso + (\alpha \cdot \alpha_r) \cdot v_{i_r} \in span((v_i)_{i \in I}) \\$

(2) Sind alle $v_i \in U$ für $i \in I,$ so gehören alle Linearkombinationen von endlich vielen Vektoren aus $(v_i)_{i \in I}$ zu U.
$\\$Denn: U Vektorraum $\Rightarrow span((v_i)_{i \in I}) \subseteq U$


## Folgerung

$span((v_i)_{i \in I})$ ist der kleinste Untervektorraum von V, der alle $v_i, i \in I,$ enthält.


## Beispiele

(1) $V = \mathbb{R}^3, \ v \in  V$ mit $v \neq 0 \\$
$span(v) = \{ \alpha \cdot v | \alpha \in \mathbb{R} \}$ ist die Gerade durch den Nullpunkt, die den Vektor v enthält $\\$

(2) $V = \mathbb{R}^3, \ u,v \in  V$ mit $u \neq 0, \ v \neq 0$ und $u \notin span(v) \\$
$span(u,v) = \{ \alpha \cdot u + \beta \cdot v \ | \ \alpha, \beta \in \mathbb{R} \}$ ist die Ebene durch den Nullpunkt, die u und v entält. $\\$

(3) In $K^n$ betrachten wir die Familie $(e_i)_{i=1,\dotso,n}$ mit $e_i = \begin{pmatrix}
0 \\
\vdots \\
0 \\
1 \\
0 \\
\vdots \\
0 \\
\end{pmatrix},$ wobei die 1 an der i-ten Stelle steht.
Dann ist $span((e_i)_{i=1,\dotso,n}) = K^n \\$
Denn: $x = \begin{pmatrix}
x_1 \\
\vdots \\
x_n \\
\end{pmatrix}
\in K^n \Rightarrow x = x_1 \cdot e_1 + \dotso + x_n \cdot e_n$


## Definition 3.3

Sei V ein K-Vektorraum und $U \subseteq V$ ein Untervektorraum. Eine Familie $(v_i)_{i \in I}$ von Vektoren aus V heißt ein $\textbf{Erzeugendensystem}$ von U, wenn $U~=~span((v_i)_{i \in I}).$ U heißt $\textbf{endlich \ erzeugt,}$ wenn es für U ein endliches Erzeugendensystem $(vi)_{i\in I}) = (v_1, \dotso, v_n)$ gibt.


## Bemerkung

Ein Vektor u heißt $\textbf{eindeutig darstellbar}$ als Linearkombination der Vektoren $v_1, \dots, v_r$, wenn $u \in span(v_1, \dotso, v_r)$ ist und gilt: $\\u = \sum\limits_{i=1}^r \alpha_i \cdot v_i \text{ und } u = \sum\limits_{i=1}^r \beta_i \cdot v_i \ \Rightarrow \alpha_i = \beta_i \ \forall \ i = 1, \dotso, r$


## Beispiel

Sei $V = \mathbb{R}^3$ und $U = span\{v_1 = \begin{pmatrix}
1\\ 1\\ -1\\ \end{pmatrix}, v_2 = \begin{pmatrix}
1\\ 0\\ 1\\ \end{pmatrix}, v_3 = \begin{pmatrix}
3\\ 1\\ 1\\ \end{pmatrix}\}.\\$

Für $t \in \mathbb{R}$ beliebig gilt dann $-t \cdot v_1 - 2 \cdot t \cdot v_2 + t \cdot v_3 = \begin{pmatrix}
- t - 2 \cdot t + 3 \cdot t \\
- t - 0 + t \\
t - 2 \cdot t + t \\
\end{pmatrix}
= \begin{pmatrix} 0\\ 0\\ 0\\ \end{pmatrix} \\$

Das bedeutet: Jeder Vektor $u = \alpha_1 \cdot v_1 + \alpha_2 \cdot v_2 + \alpha_3 \cdot v_3 \in U = span(v_1,v_2,v_3)$ lässt sich auf unendlich viele Arten als Linearkombination von $v_1,v_2,v_3$ darstellen, nämlich: $u = (\alpha_1 - t) \cdot v_1 + (\alpha_2 - 2 \cdot t) \cdot v_2 + (\alpha_3 + t) \cdot v_3$ mit $t \in \mathbb{R}$ beliebig. $\\$

Grund: Erzeugendensystem ist zu groß $\\$
Behauptung: $span(v_1,v_2) = span(v_1,v_2,v_3)$ $\\$
Beweis: $\\$
$v_1,v_2 \in span(v_1,v_2,v_3) \xRightarrow{3.1} span(v_1,v_2) \subseteq U\\$
$v_3 = v_1 + 2 \cdot v_2 \Rightarrow v_1,v_2,v_3 \in span(v_1,v_2) \\ \xRightarrow{3.1} U = span(v_1,v_2,v_3) \subseteq span(v_1,v_2) \ \checkmark\\$
Insgesamt folgt: $U = span(v_1,v_2)$

Jetzt gilt: Jeder Vektor $u \in U$ lässt sich eindeutig als Linearkombination von $(v_1,v_2)$ darstellen. $\\$

Sei $u = \alpha_1 \cdot v_1 + \alpha_2 \cdot v_2 und u = \beta_1 \cdot v_1 + \beta_2 \cdot v_2.$ Dann gilt: $\\$
$\alpha_1 \cdot \begin{pmatrix} 1 \\ 1\\ -1\\ \end{pmatrix} + \alpha_2 \cdot \begin{pmatrix} 1\\ 0\\ 1\\ \end{pmatrix} = \beta_1 \cdot \begin{pmatrix} 1 \\ 1\\ -1\\ \end{pmatrix} + \beta_2 \cdot \begin{pmatrix} 1\\ 0\\ 1\\ \end{pmatrix} \\$
$\Rightarrow \begin{pmatrix} \alpha_1 + \alpha_2 \\ \alpha_1 \\ -\alpha_1 + \alpha_2 \end{pmatrix} = \begin{pmatrix} \beta_1 + \beta_2 \\ \beta_1 \\ -\beta_1 + \beta_2 \end{pmatrix} \\$
$\Rightarrow \alpha_1 = \beta_1 \text{ und } \alpha_2 = \beta_2$


### Vorüberlegung

Sei $U = span(v_1, \dotso, v_n)$ und seien für einen Vektor $u \in U$ zwei Darstellungen als Linearkombination gegeben: $u = \sum\limits_{i=1}^n \alpha_i \cdot v_i$ und $u = \sum\limits_{i=1}^n \beta_i \cdot v_i.\\$
Dann ist $0 = u-u = \sum\limits_{i=1}^n (\alpha_i - \beta_i) \cdot v_i.$
Dies ist eine Darstellung des Nullvektors 0 als Linearkombination der $v_i.\\$

Andererseits gilt immer $0 = 0 \cdot v_1 + \dotso + 0 \cdot v_n.$ Hat der Nullvektor nur diese Darstellung, so muss dann gelten:
$\\ (\alpha_i - \beta_i) = 0 \ \forall \ i=1,...,n \ \iff \ \alpha_i = \beta_i \ \forall \ i=1,...,n.\\$
Ergebnis: Ist der Nullvektor eindeutig als Linearkombination von $v_1,...,v_n$ darstellbar, so auch jeder beliebige Vektor $u \in U.$


## Definition 3.4

Sei V ein K-Vektorraum und $(v_1,...,v_n)$ eine Familie von Vektoren aus V. Die Familie $(v_1,...,v_n)$ heißt $\textbf{linear unabhängig,}$ wenn gilt:
$\\ \alpha_1 \cdot v_1 + ... +\alpha_n \cdot v_n = 0 \Rightarrow \ \alpha_1 = 0, ... , \alpha_n = 0.$ 


Allgemein heißt eine Familie $(v_i)_{i \in I}$ von Vektoren aus V $\textbf{linear unabhängig,}$ wenn jede endliche Teilfamilie von $(v_i)_{i \in I}$ linear unabhängig ist.


Eine Familie $(v_i)_{i \in I}$ heißt $\textbf{linear abhängig,}$ wenn es eine endliche Teilfamilie $(v_{i_1},...,v_{i_n})$ gibt, sodass: $\\$
Es gibt Skalare $\alpha_1,...\alpha_n \in K,$ die nicht alle 0 sind, sodass $\alpha_1 \cdot v_1 +...+ \alpha_n \cdot v_n = 0.$


### Vereinbarung

Statt "die Familie $(v_1,...,v_n)$ ist linear (un-) abhängig" sagen wir kurz "die Vektoren $v_1,...,v_n$ sind linear (un-) abhängig."


## Lemma 3.5

Für eine Familie $(v_i)_{i \in I}$ von Vektoren eines K-Vektorraums V sind äquivalent:
(1) $(v_i)_{i \in I}$ ist linear unabhängig $\\$
(2) Jeder Vektor $u \in span((v_i)_{i \in I})$ ist eindeutig als Linearkombination von Vektoren aus $(v_i)_{i \in I}$ darstellbar.


Beweis: $\\$

(1) $\Rightarrow$ (2): Ist $u = \sum\limits_{i \in I} \alpha_i\cdot v_i$ und $u = \sum\limits_{i \in I} \beta_i \cdot v_i,$ so folgt $\sum\limits_{i \in I} \alpha_i\cdot v_i = \sum\limits_{i \in I} \beta_i \cdot v_i.$ Folglich gilt: $\sum\limits_{i \in I} \ (\alpha_i - \beta_i) \cdot v_i = 0.$ Wegen (1) gilt 
$\alpha_i - \beta_i = 0 \ \forall \ i \in I$ und damit $\alpha_i = \beta_i \  \forall \ i \in I.$

(2) $\Rightarrow$ (1): Wegen (2) ist insbesondere der Nullvektor eindeutig als Linearkombination von Vektoren aus $(v_i)_{i \in I}$ darstellbar, d.h. ist 
$\alpha_i \cdot v_{i_1} + \alpha_n \cdot v_{i_n} = 0$ für $v_{i_1},...,v_{i_n} \in (v_i)_{i \in I},$ so gilt $\alpha_1 = 0,..., \alpha_n = 0,$ d.h. $(v_i)_{i \in I}$ ist linear unabhängig. $\\$


## Beispiel

Sei V ein K-Vektorraum. Dann gilt: $\\$
(1) Für $v \in V$ gilt: $v \neq 0 \iff$ v linear unabhängig $\\$
(2) Eine Familie von Vektoren, zu der der Nullvektor gehört, ist linear abhängig.
(3) Ist $n \geq 2,$ so ist eine Familie $(v_1,...,v_n)$ von Vektoren aus V genau dann linear abhängig, wenn sich einer der Vektoren als Linearkombination der übrigen darstellen lässt.


## Defintion 3.7

Eine Familie $\mathcal{B} = (v_i)_{i \in I}$ in einem K-Vektorraum V heißt eine $\textbf{Basis}$ von V, wenn gilt: $\\$
$(\mathcal{B}1) \ \mathcal{B}$ ist ein Erzeugendensystem von V $\\$
$(\mathcal{B}2) \ \mathcal{B}$ ist linear unabhängig $\\$

Ist $\mathcal{B}$ eine Basis aus n Vektoren, so heißt n die $\textbf{Länge der Basis.}$


## Beispiel

(1) $\mathcal{K} = (e_1,...,e_n)$ ist eine Basis von $K^n$ der Länge n. Sie heißt die kanonische Basis von $K^n.\\$
(2) Sei $K^{m \times n}$ der K-Vektorraum der Matrizen vom Typ (m,n) mit Einträgen aus K. Dann bilden die $m \cdot n$ Elementarmatrizen $E_{ij} \sim$ (m,n) eine Basis von $K^{m \times n}$ der Länge $m \cdot n. \\$
Für $1 \leq i \leq m, \ 1 \leq j \leq n$ heißt die Matrix $E_{ij} \sim$ (m,n), welche an der Stelle (i,j) den Eintrag 1 und sonst überall 0 hat, eine $\textbf{Elementarmatrix,}$ z.B. $E_{23} = \begin{pmatrix} 0&0&0&0 \\ 0&0&1&0 \\ 0&0&0&0 \end{pmatrix} \sim$ (3,4).


## Satz 3.8

Sei V ein K-Vektorraum und $\mathcal{B} = (v_1,...,v_n)$ eine endliche Familie von Vektoren aus V. Dann sind folgende Aussagen äquivalent: $\\$
(1) $\mathcal{B}$ ist eine Basis. $\\$
(2) $\mathcal{B}$ ist ein unverkürzbares Erzeugendensystem von V. $\\$
(3) $\mathcal{B}$ ist ein Erzeugendensystem mit der zusätzlichen Eigenschaft, dass es zu jedem $v \in V$ eindeutig bestimmte Skalare  $\alpha_1,...,\alpha_n \in K$ gibt, sodass $\\ v = \alpha_1 \cdot v_1+...+ \alpha_n \cdot v_n$ gilt. $\\$
(4) $\mathcal{B}$ ist unverlängerbar linear unabhängig.

Beweis: durch Ringschluss $\\$

$(1) \ \Rightarrow (2): \ \mathcal{B}$ Basis $\Rightarrow$ $\mathcal{B}$ linear unabhängig $\xRightarrow{3.6  (3)  }$ Kein Vektor $v_i \in \mathcal{B}$ lässt sich als Linearkombination der anderen Vektoren aus $\mathcal{B}$ darstellen 
$\Rightarrow$ Für i = 1,...,n ist $\mathcal{B} \setminus \{v_i \}$ kein Erzeugendensystem mehr. Da $\mathcal{B}$ als Basis ein Erzeugendensystem ist, ist $\mathcal{B}$ also ein unverkürzbares Erzeugendensystem. $\\$

$(2) \Rightarrow (3): \ \mathcal{B}$ Erzeugendensystem $\Rightarrow$ Jeder Vektor $v \in V$ hat eine eindeutige Darstellung $v = \sum\limits_{i=1}^n \alpha_i \cdot v_i. \\$
Angenommen, die Eindeutigkeitseigenschaft gilt nicht. $\\$
Betrachte  $v = \sum\limits_{i=1}^n \alpha_i \cdot v_i$ und $v = \sum\limits_{i=1}^n \beta_i \cdot v_i$ mit $\alpha_i \neq \beta_i$ für mindestens ein $i \in \{1,...,n \}.$ O.B.d.A. sei $\alpha_1 \neq \beta_1.$ Subtraktion und Auflösung nach $v_1$ liefern: $\\ v = \sum\limits_{i=1}^n (\alpha_i - \beta_i) \cdot v_i = 0.$ Da $\alpha_1 - \beta_1 \neq 0,$ folgt: $v_1 = -\frac{\alpha_2 - \beta_2}{\alpha_1 - \beta_1} \cdot v_2 - ... - \frac{\alpha_n - \beta_n}{\alpha_1 - \beta_1} \cdot v_n \\ \Rightarrow v_1 \in span(v_2,...,v_n) \Rightarrow \mathcal{B}$ ist verkürzbar $\lightning$ zu (2). $\\$

$(3) \Rightarrow (4):$ Wegen der Eindeutigkeitseigenschaft ist $\mathcal{B}$ nach 3.5 linear unabhängig. Sei $v \in V$ beliebig. Nach (3) gibt es $\alpha_1,...,\alpha_n,$ sodass $\\ v = \alpha_1 \cdot v_1 + ... + \alpha_n \cdot v_n. \Rightarrow \ (-1) \cdot v + \alpha_1 \cdot v_1 + ... + \alpha_n \cdot v_n = 0$ und nicht alle Koeffizienten sind 0 $\Rightarrow \mathcal{B} \cup \{ v \} = (v,v_1,...,v_n)$ ist linear abhängig. $\\$
Also ist $\mathcal{B} = (v_1,...,v_n)$ unverlängerbar linear unabhängig.  $\\$

$(4) \Rightarrow (1):$ Nach (4) ist $(v_1,...,v_n)$ linear unabhängig und für jedes $v \in V$ ist $(v,v_1,...,v_n)$ linear abhängig $\Rightarrow$ Es existieren $\alpha, \alpha_1,...,\alpha_n \in K$ mit $\\ \alpha \cdot v +\alpha_1 \cdot v_1 + ... + \alpha_n \cdot v_n = 0,$ wobei nicht $\alpha$ und alle $\alpha_i$ gleich 0 sind. Wäre $\alpha = 0,$ dann wären alle $\alpha_i = 0$, weil $v_1,...,v_n$ linear unabhängig sind. Also muss $\alpha \neq 0$ sein. $\\$
$\Rightarrow v = - \frac{\alpha_1}{\alpha} \cdot v_1 -...- \frac{\alpha_n}{\alpha} \cdot v_n \Rightarrow v \in span(v_1,...,v_n) \Rightarrow \mathcal{B}$ Erzeugendensystem von V $\Rightarrow \mathcal{B}$ Basis.


## Folgerung

Ist V nicht endlich erzeugt, so gibt es eine unendliche linear unabhängige Familie in V.


## Satz 3.9: Basisauswahlsatz

Aus jedem endlichen Erzeugendensystem eines Vektorraums kann man eine Basis auswählen. Insbesondere hat jeder endlich erzeugte Vektorraum eine endliche Basis.

Beweis: $\\$
Von dem endlichen Erzeugendensystem nehme man so lange nacheinander Vektoren weg, bis ein unverkürzbares Erzeugendensystem entsteht. Dieses ist nach 3.8 eine Basis. Sie ist endlich, weil das Erzeugendensystem endlich ist.


## Satz 3.10

Jeder Vektorraum besitzt eine Basis.


## Lemma 3.11: Austauschlemma von Steinitz

Sei V ein K-Vektorraum und $\mathcal{B} = (v_1,.,,,v_n)$ eine Basis in V. Ist dann $\\ w = \alpha_1 \cdot v_1 +...+ \alpha_k \cdot v_k +...+ \alpha_n \cdot v_n$ und $\alpha_k \neq 0,$ so ist $\\ \mathcal{B}' = (v_1,...,v_{k-1},w,v_{k+1},...v_n)$ wieder eine Basis von V.

Beweis: $\\$
O.B.d.A. sei $\alpha_1 \neq 0$ in $w = \alpha_1 \cdot v_1 +...+ \alpha_n \cdot v_n.\ Zz: \mathcal{B}'$ ist Erzeugendensystem. $\\$

$(1) \ Zz: \mathcal{B}' = (w,v_2,...,v_n)$ ist Erzeugendensystem. $\\$
$v \in V \xRightarrow{\mathcal{B} Basis}$ Es existieren $\gamma_1,...,\gamma_n$ mit $v = \gamma_1 \cdot v_1 +...+\gamma_n \cdot v_n.$ Wegen $\alpha_1 \neq 0$ gilt $v_1 = \frac{1}{\alpha_1} \cdot w - \frac{\alpha_2}{\alpha_1} \cdot v_2 - ... - \frac{\alpha_n}{\alpha_1} \cdot v_n$ und damit $\\ v = \frac{\gamma_1}{\alpha_1} \cdot w + (\gamma_2 - \gamma_1 \cdot \frac{\alpha_2}{\alpha_1}) \cdot v_2 +...+ (\gamma_n - \gamma_1 \cdot \frac{\alpha_n}{\alpha_1}) \cdot v_n \\$
$(2) \ Zz: \mathcal{B}'$ istlinear unabhängig. $\\$
$\beta \cdot w + \beta_2 \cdot v_2 +...+ \beta_n \cdot v_n = 0$ und $w = \alpha_1 \cdot v_1 +...+ \alpha_n \cdot v_n \Rightarrow \beta \cdot \alpha_1 \cdot v_1 + (\beta \cdot \alpha_2 + \beta_2) \cdot v_2 +...+ (\beta \cdot \alpha_n + \beta_n) \cdot v_n = 0.$ Da $\mathcal{B}$ linear unabhängig, folgt: $\beta \cdot \alpha_1 = 0$ und $\beta \cdot \alpha_i + \beta_i = 0$ für i = 2,...,n. Da $\alpha_1 \neq 0,$ folgt $\beta = 0$ und damit $\beta_i = 0$ für i 0 2,...,n. Folglich ist $(w,v_2,...,v_n)$ linear unabhängig.


## Satz 3.12: Austauschsatz

Sei V ein K-Vektorraum und $\mathcal{B} = (v_1,...v_n)$ eine Basis von V und 
$(w_1,...,w_r)$ eine linear unabhängige Familie in V. Dann gilt: $\\$
$(1) \ r \leq n \\$
$(2)$ Es gibt Indizes $i_1,...,i_r \in \{1,..,n\},$ sodass man nach Austausch von $v_{i_1}$ gegen $w_1,$ $v_{i_2}$ gegen $w_2,$ ..., $v_{i_r}$ gegen $w_r,$ wieder eine Basis von V erhält.


## Bemerkung

Umnummerieren der Vektoren $\mathcal{B}^* = (w_1,...,w_r,v_{r+1},...,v_n)$


Beweis von Satz 3.12: durch vollständige Induktion nach r $\\$
$(IA)$ r = 0: Es ist nichts zu zeigen. $\\$
$(IS): \ r-1 \mapsto r:$ Sei $(w_1,...,w_r)$ linear unabhängig. Folglich ist $(w_1,...,w_{r-1})$ auch linear unabhängig. Nach IV ist 
$(w_1,...,w_{r-1},v_r,...,v_n)$ eine Basis von V und es gilt $r-1 \leq n \\$

$\bullet$ Wegen $r-1 \leq n,$ muss gezeigt werden: $r-1 < n.$ Wäre $r-1 = n,$ so wäre $(w_1,...,w_{r-1})$ eine Basis von V. Nach 3.8 wäre $(w_1,...,w_{r-1})$ unverlängerbar linear unabhängig $\lightning$ zu $(w_1,...,w_{r-1},w_r)$ linear unabhängig. Also ist $r-1 < n.$ Daraus folgt $r \leq n.\\$

$\bullet$ Da $(w_1,...,w_{r-1},v_r,...,v_n)$ Basis von V, gibt es 
$\alpha_1,...,\alpha_n \in K,$ sodass $\\ w_r = \alpha_1 \cdot w_1 +...+\alpha_{r-1} \cdot w_{r-1} + \alpha_r \cdot v_r +...+ \alpha_n \cdot v_n.$ Wäre 
$\alpha_r = 0,..., \alpha_n = 0,$ so wäre $w_r$ eine Linearkombination von $w_1,...,w_{r-1} \lightning$ zu $(w_1,...,v_r)$ linear unabhängig. Also ist mindestens ein Element von $\{ \alpha_r,..., \alpha_n \}$ ungleich 0. O.B.d.A. sei $\alpha_r \neq 0.$ Austauschlemma von Steinitz mit 
$(w_1,...,w_{r-1},v_r,...,v_n): \\ \mathcal{B}^* = (w_1,...,w_{r-1},w_r,v_{r+1},...,v_n)$ ist Basis von V.


## Korollar A

Sei V ein K-Vektorraum mit einer endlichen Basis. Dann gilt: $\\$
$(1)$ Jede Basis von V ist endlich. $\\$
$(2)$ Je zwei Basen von V haben dieselbe Länge.


## Definition 3.13

Sei V ein K-Vektorraum. $\\$
$(1)$ Hat V eine Basis der Länge n, so heißt diese allen Basen von V gemeinsame Länge n die $\textbf{Dimension}$ von V. Man schreibt: $dim_KV = n. \\$
$(2)$ Hat V keine Basis endlicher Länge, so definiert man: $dim_KV = \infty.$


## Korollar B

Ist V ein endlich erzeugter K-Vektorraum und $U \subseteq V$ ein Untervektorraum, so ist auch U endlich erzeugt und es gitl: $dim_KU \leq dim_KV.$ Weiter gilt: $dim_KU = dim_KV \Rightarrow U = V.$


## Satz 3.14: Basisergänzungssatz

Sei V ein K-Vektorraum und $dim_KV = n.$ Sei $(w_1,...,w_r)$ eine linear unabhängige Familie in V und $r < n.$ Dann kann man Vektoren $w_{r+1},...,w_n \in V$ so finden, dass $(w_1,...,w_r,w_{r+1},...,w_n)$ eine Basis von V ist.

Beweis: $\\$
Erzeugendensystem $(v_1,..,v_m)$ mit $m \geq n \Rightarrow$ Basisauswahlsatz 3.9 $\\ \Rightarrow$ Austauschsatz 3.12


## Lemma 3.15

Sei V ein K-Vektorraum und seien $U,W \subseteq V$ Untervektorräume. Dann gilt: 
$\\$
$(1)$ $U \cap W$ ist Untervektorraum von V $\\$
$(2)$ $U+W = \{ v \mid v=u+w$ mit $u \in U, \ w \in W \}$ ist Untervektorraum von V


## Lemma 3.16

Sei V = U+W. Dann sind folgende Bedingungen äquivalent: $\\$
$(1)$ $U \cap W = \{0\} \\$
$(2)$ Jeder Vektor $v \in V$ hat eine eindeutige Darstellung $v=u+w$ mit $u \in U, w \in W.$

Beweis: $\\$
$(1) \Rightarrow (2):$ Sei $v=u+w$ und $v=u'+w'.$ Dann gilt: $\\ 0 = v-v = (u+w)-(u'+w') = (u-u')+(w-w') \Rightarrow \underbrace{u-u'}_{\in U} = \underbrace{w'-w}_{\in W} \\ \Rightarrow u-u' = 0 = w'-w,$ da $U \cap W = \{0\} \Rightarrow u=u'$ und $w=w' \\$
$(2) \Rightarrow (1):$ Angenommen, $U \cap W \neq \{0\}.$ Dann existiert $x \in U \cap W$ mit $x \neq 0 \Rightarrow x = x+0 \in U+W$ und $x = 0+x \in U+W$ sind verschiedene Darstellungen von x $\lightning$ zu (2).


## Definition 3.17

Sei V ein K-Vektorraum und seien $U,W \subseteq V$ Untervektorräume. Dann heißt V die $\textbf{direkte Summe}$ von U und W (in Zeichen: $U \bigoplus W),$ wenn jeder Vektor $v \in V$ sich eindeutig als Summe $v=u+w$ von Vektoren $u \in U$ und $w \in W$ darstellen lässt. Entsprechend ist die direkte Summe $V = U_1 \bigoplus ... \bigoplus U_r$ von Untervektorräumen $U_1,...,U_r$ definiert.


## Folgerung A

Sei V ein K-Vektorraum und seien $U,W \subseteq V$ Untervektorräume. Dann gilt: 
$\\ V = U \bigoplus W \iff V = U+W$ und $U \cap W = \{0\}.$


## Folgerung B: Dimensionsformel für direkte Summen

Sei V ein K-Vektorraum und seien $U,W \subseteq V$ Untervektorräume. Dann gilt:
$\\ V = U \bigoplus W \Rightarrow dim_KV = dim_KU + dim_KW.$


## Korollar

Ist V ein endlich-dimensionaler K-Vektorraum und $W \subseteq V$ ein Untervektorraum, so gibt es zu W einen (i.A. nicht eindeutig bestimmten) Untervektorraum W' von V, sodass $V = W \bigoplus W'.$ W' heißt dann direkter Summand von V zu W.

Beweis: $\\$
Wir wählen eine Basis $(v_1,...,v_m)$ von W und ergänze sie zu einer Basis 
$(v_1,...,v_m,v_{m+1},...,v_n)$ von V. Dann sei $W' = span(v_{m+1},...,v_n).$ Da jeder Vektor $v \in V$ eine eindeutige Darstellung $v = \sum\limits_{i=1}^n \alpha_i \cdot v_i = \sum\limits_{i=1}^m \alpha_i \cdot v_i + \sum\limits_{i=m+1}^n \alpha_i \cdot v_i$ hat, ist $V = W \bigoplus W'.$


## Beispiel
$V = \mathbb{R}^3,~U = span \bigg(\begin{pmatrix} 0\\ 1 \end{pmatrix}\bigg),~W = span \bigg(\begin{pmatrix} 2\\ 1 \end{pmatrix}\bigg) \Rightarrow V = U \bigoplus W$