# 1. Vektorräume und lineare Abbildungen

##Definition 1.1
Sei $K$ ein Körper (z.B. $K=\mathbb{R}$), $V$ eine nichtleere Menge. Auf $V$ seien zwei Verknüpfungen definiert, und zwar:

- eine innere Verknüpfung $+:V \times V \to V, (u,v) \mapsto u+v$, die als Addition bezeichnet wird
- eine äußere Verknüpfung $\cdot: K \times V \to V, (\alpha, v) \mapsto \alpha \cdot v$, die als Multiplikation mit Skalaren bezeichnet wird.

$V$ mit diesen Verknüpfungen heißt K-Vektorraum (KVR), wenn folgende Axiome gelten:

(V1) $V$ ist bzgl. der Addition eine abelsche Gruppe, d.h. es gilt:

(G1) $(u+v)+w=u+(v+w)$ für alle $u,v,w \in V \\$
(G2) Es existiert ein neutrales Element $0 \in V$ mit $0+v=v=v+0$ für alle $v \in V \\$
(G3) Zu jedem $v \in V$ existiert ein "negatives Element" $-v \in V$, sodass $v+(-v)=0 \\$
(G4) $u+v=v+u$ für alle $u,v \in V$

(V2) Die Multiplikation mit Skalaren ist verträglich mit der Addition in $V$ und mit den Operationen in $K$, d.h. für alle $u,v \in V$ und $\alpha, \beta, 1 \in K$ gilt:

(a) $( \alpha + \beta) \cdot v= \alpha \cdot v + \beta \cdot v$
(b) $\alpha \cdot (u+v) = \alpha \cdot u + \alpha \cdot v$
(c) $\alpha \cdot (\beta \cdot v) = (\alpha \cdot \beta) \cdot v$
(d) $1 \cdot v = v$

Die Elemente von $V$ heißen Vektoren, die Elemente von $K$ heißen Skalare, $0 \in V$ heißt Nullvektor.
Vereinbarung: statt $u+(-v)$ schreibt man $u-v$.

##Satz 1.2
In einem KVR $V$ gelten folgende Rechenregeln:

(1) $0 \cdot u = 0$ für alle $u\in V$
(2) $\alpha \cdot 0 = 0$ für alle $\alpha \in K$
(3) $\alpha \cdot u = 0 \implies \alpha=0$ oder $u=0$
(4) $( - 1 ) \cdot u = -u$ für alle $u \in V$

###Beweis
(1) $0 \cdot u  \overset{\text{G2}}{\underset{\text{Körper}}{=}}  (0+0) \overset{V2(a)}{=} 0 \cdot u + 0 \cdot u \\$
Addition des Negativen liefert: $\\$
$0 = (-0 \cdot u + 0 \cdot u) + 0 \cdot u = 0+0 \cdot u = 0 \cdot u$
(2) siehe Übungsaufgaben
(3) siehe Übungsaufgaben
(4) $u+(-1) \cdot u \overset{V2(d)}{=} 1 \cdot u + (-1) \cdot u \overset{V2(a)}{=} (1-1) \cdot u = 0 \cdot u \overset{(1)}{=} 0 \implies (-1) \cdot u = -u$

###Beispiele
(1) Das Standardbeispiel eines KVRs ist der sogenannte Standardraum $K^n=\{ x = \begin{pmatrix} x_{1} \\ \vdots \\ x_{n}\end{pmatrix}| x_{i} \in K$ für $i=1,...,n \}$ der geordneten $n$-Tupel von Skalaren $x_{i} \in K$. Die $x_{i}$ heißen Komponenten des Vektors $x$.

###Bemerkung
Geordnet bedeutet, dass die Reihenfolge der Komponenten wichtig ist:
$\begin{pmatrix}
  x_{1} \\
  \vdots \\
  x_{n}
\end{pmatrix} =
\begin{pmatrix}
  y_{1} \\
  \vdots \\
  y_{n}
\end{pmatrix} \iff x_{1} = y_{1}, ... , x_{n} = y_{n}$

Addition im $K^n:
\begin{pmatrix}
  x_{1} \\
  \vdots \\
  x_{n}
\end{pmatrix} +
\begin{pmatrix}
  y_{1} \\
  \vdots \\
  y_{n}
\end{pmatrix} =
\begin{pmatrix}
  x_{1} + y_{1} \\
  \vdots \\
  x_{n} + y_{n}
\end{pmatrix}$

Multiplikation mit Skalaren im $K^n : \alpha \cdot
\begin{pmatrix} x_{1} \\ \vdots \\ x_{n} \end{pmatrix} = \begin{pmatrix} \alpha \cdot x_{1} \\ \vdots  \\\alpha \cdot x_{n} \end{pmatrix}$

(2) Vektorraum der Matrizen

##Definition 1.3
Sei $K$ ein Körper (z.B. $K=\mathbb{R}$). Für $m,n \in \mathbb{N}$ seien $m$ Zahlenreihen aus jeweils $n$ Zahlen aus $K$ gebildet und die $m$ Zahlenreihen so untereinander geschrieben, dass die Zahlen in Form eines Rechtecks durch Klammern zu einem neuen Objekt zusammengefasst werden. Das Schema $A = \begin{pmatrix}  a_{11} & \cdots & a_{1n} \\ \vdots & & \vdots \\ a_{m1} & \cdots & a_{mn} \end{pmatrix}$ heißt dann eine Matrix vom Typ $(m,n)$. Die $a_{ij}$ nennt man allgemein die Einträge der Matrix.

Schreibenweisen:
$A \sim (m,n)$
$A= (a_{ij}) \sim (m,n)$
$A= (a_{ij})_{1 \leq i \leq m, 1 \leq j \leq n}$

Die Menge der Matrizen $A \sim (m,n)$ mit Einträgen aus K bezeichnet man mit $K^{(m,n)}: K^{(m,n)} = \{ A = \begin{pmatrix} a_{11} & \cdots & a_{1n} \\ \vdots & & \vdots \\ a_{m1} & \cdots & a_{mn} \end{pmatrix} | a_{ij} \in K$ für $1 \leq i \leq m, 1 \leq j \leq n \}$.

$K^{(m,n)}$ ist ein KVR, wenn man definiert:

Additions: $A=(a_{ij}) \sim (m,n), B=(b_{ij} \sim (m,n) \\
A+B=(a_{ij} + b_{ij}) \sim (m,n)$

Multiplikation mit Skalaren: $A=(a_{ij}) \sim (m,n), \alpha \in K \\
\alpha \cdot A = (\alpha \cdot a_{ij}) \sim (m,n)$

(3) Sei $M~\neq~\emptyset$ eine beliebige Menge, $K$ ein Körper. Dann ist $Abb(M,K)=\{f:M \to K | f~Abbildung\}$ ein KVR, wenn man definiert:

Addtion: $f,g:M \to K$

$f+g:M \to K, (f+g)(x)=f(x)+g(x)$

Multiplikation mit Skalaren: $f:M \to K, \alpha \in K$

$\alpha \cdot f: M \to  K, (\alpha \cdot f)(x) = \alpha \cdot f(x).$

##Definition 1.4
Sei $V$ ein KVR. Eine Teilmenge $U \subseteq V$ heißt Untervektorraum (UVR) von $V$, wenn sie mit der von $V$ induzierten Addition und Mulitplikation mit Skalaren einen KVR bildet.

##Satz 1.5
Sei $V$ ein KVR und $U \subseteq V. U$ ist genau dann ein UVR von $V$, wenn gilt:

(UV1) $U \neq \emptyset \\$
(UV2) $u,v \in U \implies u+v \in U$ (d.h. $U$ ist abgeschlossen gegenüber der in $V$ induzierten Addition) $\\$
(UV3) $u \in U, \alpha \in K \implies \alpha \cdot u \in U$ (d.h. U ist abgeschlossen gegenüber der in $V$ induzierten Mulitplikation mit Skalaren)

###Beweis
$"\Longleftarrow"$: Es gelten die (UVi). Zz: $U$ ist UVR. Wegen (UV2) ist die Einschränkung der Addition $+: V \times V \to  V$ auf $U \times U$ eine inere Verknüpfung $+: U \times U \to U$ auf U$. Zz: $U$ ist bzgl. + eine abelsche Gruppe:

(G1) Assoziativgesetz gilt, weil es in $V$ gilt. $\\$
(G2) Nach (UV1) ist $U \neq \emptyset$, d.h. es existiert $u \in U \overset{UV3}{\implies} 0 \cdot u = 0 \in U \\$
(G3) $u \in U$ beliebig $\implies -u \overset{1.2}{=}(-1) \cdot u \overset{UV3}{\in} U \\$
(G4) Kommutativgesetz gilt, weil es in $V$ gilt

Wegen (UV3) ist die Einschränkung der Multiplikation mit Skalaren $\cdot: K \times V \to V$ auf $K \times V$ eine äußere Verknüpfung $\cdot : K \times U \to U$ auf $U$. Die Axiome (V2) gelten in $U$, weil sie in $V$ gelten.

$"\Longrightarrow"$: Sei $U$ ein UVR von $V$. Dann gilt (UV1), weil z.B. $0 \in U$ gelten muss (nach G2).

(UV2), weil $+:U \times U \to U$ eine innere Verknüpfung auf $U$ ist. $\\$
(UV3), weil $\cdot: K \times U \to U$ eine äußere Verknüpfung auf $U$ ist.

##Defintion 1.6
Seien $V$ und $W$ Vektorräume über demselben Körper $K$. Eine Abbildung $f: V \to W$ heißt lineare Abbildung (genauer $K$-lineare Abbildung), wenn sie mit der Vektorraumstruktur verträglich ist, d.h. wenn gilt:

(L1) $f(u+v)=f(u)+f(v)$ für alle $u,v \in V \\$
(L2) $f(\alpha \cdot v)=\alpha \cdot f(v)$ für alle $\alpha \in K, v \in V$

Kurz: (L) $f(\alpha \cdot u + \beta \cdot f(v)$ für alle $\alpha, \beta \in K$ und $u,v \in V$

###Ergänzung
Seien $V$ und $W$ Vektorräume über $K$. Eine $K$-lineare Abbildung $f:V \to W$ heißt auch Homomorphismus. Speziell heißt eine $K$-lineare Abbildung $f:V \to W$ ein

- Isomorphismus, wenn $f$ bijektiv
- Endomorphismus, wenn $V=W$
- Automorphismus, wenn $f$ bijektiv und $V=W$

##Definition 1.7
Wei folgt ist eine Multiplikation von Matrizen $A \in K^{(m,n)}$ mit Vektoren aus $K^n$ definiert.

$A \cdot x =
\begin{pmatrix}
a_{11} & \cdots & a_{1n}
\\ \vdots & & \vdots
\\ a_{m1} & \cdots & a_{mn}
\end{pmatrix}
\cdot
\begin{pmatrix} x_{1}
\\ \vdots
\\ x_{n}
\end{pmatrix}
=
\begin{pmatrix}
a_{11} \cdot x_1 + \cdots + a_{1n} \cdot x_n
\\ \vdots
\\ a_{m1} \cdot x_1 + \cdots + a_{mn} \cdot x_n
\end{pmatrix}
\in K^m$

###Beispiel
$\begin{pmatrix} 1 & -1 & 2 \\ 2 & 0 & 1 \end{pmatrix} \cdot \begin{pmatrix} 1 \\ 2 \\ 3 \end{pmatrix} = \begin{pmatrix} 1 \cdot 1 &+ (-1) \cdot 2 &+ 2 \cdot 3 \\ 2 \cdot 1 &+ 0 \cdot 2 &+ 1 \cdot 3 \end{pmatrix} = \begin{pmatrix} 5 \\ 5 \end{pmatrix}$

##Lemma 1.8
Jede Matrix $A \in K^{m,n}$ definiert eine lineare Abbildung $A: K^n \to K^m$ durch $x \mapsto A \cdot x.$

###Beweis
$A \cdot (\alpha \cdot x + \beta \cdot y)
=
\begin{pmatrix}
  a_{11} & \cdots & a_{1n} \\
  \vdots & & \vdots \\
  a_{m1} & \cdots & a_{mn}
\end{pmatrix}
\cdot
\begin{pmatrix}
  \alpha \cdot x_1 + \beta \cdot y_1 \\
  \vdots \\
  \alpha \cdot x_n + \beta \cdot y_n
\end{pmatrix} \\
=
\begin{pmatrix}
  a_{11} \cdot (\alpha \cdot x_1 + \beta \cdot y_1)+ \cdots + a_{1n} \cdot (\alpha \cdot x_n + \beta \cdot y_n) \\
  \vdots \\
  a_{m1} \cdot (\alpha \cdot x_1 + \beta \cdot y_1)+ \cdots + a_{mn} \cdot (\alpha \cdot x_n + \beta \cdot y_n)
\end{pmatrix} \\
=
\begin{pmatrix}
  \alpha \cdot (a_{11} \cdot x_1 + \cdots + a_{1n} \cdot x_n) \\
  \vdots \\
  \alpha \cdot (a_{m1} \cdot x_1 + \cdots + a_{mn} \cdot x_n)
\end{pmatrix}
+
\begin{pmatrix}
  \beta \cdot (a_{11} \cdot y_1 + \cdots + a_{1n} \cdot y_n) \\
  \vdots \\
  \beta \cdot (a_{m1} \cdot y_1 + \cdots + a_{mn} \cdot y_n)
\end{pmatrix} \\
=
\alpha \cdot A \cdot x + \beta \cdot A \cdot y$

##Lemma 1.9
Seien $V$ und $W$ Vektorräume über $K$. Die menge $Hom(V,W)=\{f:V \to W | f$ ist $K$-linear} aller $K$-lineaeren Abbildungen von $V$ nach $W$ ist ein KVR.

##Definition 1.10
Sei $f: V \to W$ eine Abbildung.

(a) $f$ heißt surjektiv $\iff \forall w \in W \exists v \in V$ mit $f(u)=w$
(b) $f$ heißt injektiv $\iff \forall v_1, v_2 \in V$ mit $f(v_1)=f(v_2)$ gilt $v_1 = v_2$
(c) $f$ heißt bijektiv $\iff f$ ist surjektiv und injektiv

###Graphische Darstellung

- $f$ surjektiv: HIER FOLGT EIN DIAGRAMM
- $f$ injektiv: HIER FOLGT EIN DIAGRAMM
- $f$ bijektiv: HIER FOLGT EIN DIAGRAMM

##Satz 1.11
Sei $f: V \to W$ eine $K$-lineare Abbildung. Dann gilt:

(1) $f(0)=0$ und $f(u-v)=f(u)-f(v) \ \forall \ u,v \in V$
(2) $f(\alpha_1 \cdot v_1 + ... + \alpha_n \cdot v_n)= \alpha_1 \cdot f(v_1) + ... + \alpha_n \cdot f(v_n) \ \forall \ \alpha_i \in K, v_i \in V$
(3) $V' \subseteq V$ UVR und $W' \subseteq W$ UVR $\implies f(V') \subseteq W$ und $f^{-1}(W') \subseteq V$ sind Untervektorräume
(4) $f: V \to W$ Isomorphismus $\implies f^{-1}: W \to V$ ist linear

###Beweis
(1) $f(0) \overset{1.2}{=} f(0 \cdot 0) \overset{L}{=} 0 \cdot f(0) \overset{1.2}{=} 0 \\$
$f(u-v) \overset{1.2}{=} f(u+(-v)) \overset{L}{=} f(u) + (-1) \cdot f(v) \overset{1.2}{=} f(u) - f(v)$

(2) klar, da wiederholte Anwendung von L

(3) $f(V') \subseteq W$ UVR   ÜBUNGSAUFGABE $\\$
$f^{-1}(W) = \{v \in V: f(v) \in W'\} \subseteq V$

(UV1) $0 \in W'$ und $f(0)=0 \implies 0 \in f^{-1}(W') \implies f^{-1}(W') \neq \emptyset \\$
(UV2) $u,v \in f^{-1}(W') \implies f(u), f(v) \in W' \implies f(u+v) = f(u) + f(v) \in W' \implies u+v \in f^{-1}(W') \\$
(UV3) $u \in f^{-1}(W'), \alpha \in K \implies f(u) \in W \implies f(\alpha \cdot u) = \alpha \cdot f(u) \in W' \implies \alpha \cdot u \in f^{-1}W' \\$
(UV4) $f:V \to W$ ist Isomorphismus, also linear und bijektiv. Da $f$ bijektiv, existiert die Abbildung $f^{-1}: W \to V. \\$

Zz: $f^{-1}: W \to V$ ist linear $\\$
$\alpha, \beta \in K$ und $w, w' \in W \implies u = f^{-1}(w), u'=f^{-1}(w') \in V \implies \alpha \cdot u + \beta \cdot w') \underset{bijektiv}{=} \alpha \cdot u + \beta \cdot u' = \alpha \cdot f^{-1}(w) + \beta \cdot f^{-1}(w')$

##Folgerung
Ist $f: V \to W$ eine lineare Abbildung, so sind $f(V) \subseteq W$ und $f^{-1}(0) \subseteq V$ Untervektorräume.

##Definition 1.12
Sei $f:V \to W$ eine lineare Abbildung. Dann heißt der Untervektorraum

- $Imf:=f(V)$ von $W$ das Bild von $f$
- $Kerf:=f^{-1}(0)$ von $V$ der Kern von $f$

###Bemerkung
Ist $A \in K^{m,n}$, so kann man $A$ nach 1.8 als Abbildung $A: K^n \to K^m$ auffassen und schreibt dann $Im(A)$ und $Ker(A)$.

Statistische Notation:

$Im(A)=R(A)$ ("range") $\\$
$Ker(A)=N(A)$ ("nullspace")

###Bemerkung
Sei $f: V \to W$ eine lineare Abbildung. Dann gilt:

(1) $f:V \to W$ surjektiv $\iff Imf=W$
(2) $f:V \to W$ injektiv $\iff Kerf=\{0\}$

##Satz 1.13
Seien $U,V$ und $W$ Vektorräume über $K$. Seien $g: U \to V$ und $f: V \to W$ lineare Abbildungen. Dann ist die Kompostion $f \circ g: U \to W$ eine lineare Abbildung.

##Beweis
$(f \circ g)(\alpha \cdot u + \beta \cdot u') = f(g(\alpha \cdot u + \beta \cdot u')) \overset{L}{=} f(\alpha \cdot g(u) + \beta \cdot g(u')) \overset{L}{=} \alpha \cdot f(g(u)) + \beta \cdot f(g(u')) = \alpha \cdot (f \circ g)(u) + \beta \cdot (f \circ g)(u')$
