---
numbersections: false
---

# 0. Grundlegendes

## Menge
Eine Menge ist eine abgegrenzte Gesamtheit von unt\\erscheidbaren Dingen. Diese heißen Elemente der Menge.

###Beschreibung von Mengen
- durch Aufzählen aller Elemente ($M=\{1,3,3,7\}$, $M=\{2,4,6,8,...\}$)
- durch eine die Elemente charakterisierende Eigenschaft $E$ ($M$={$x$|$x$ hat die eigenschaft $E$})

###Beispiel
$M$={$x$|$x$ ist eine positive, gerade und ganze Zahl}

###Symbole für spezielle Zahlenmengen
$\mathbb{N},\mathbb{N}_0,\mathbb{Z},\mathbb{R},\emptyset{} \\$
Sei $M$ eine Menge. $\\$
Dann $a \in M$ : $a$ ist Element von $M \\$
Dann $a \notin M$ : $a$ ist nicht Element von $M$

###Beispiel
$1 \in \mathbb{N}$, $\frac{2}{3} \in \mathbb{Z}$

###Teilmengen
$N, M$ seien Mengen
$N$ heißt Teilmenge von $M$, wenn jedes Element aus $N$ zu $M$ gehört:  $$N \subseteq M$$

###Beispiel
$\mathbb{N} \subseteq \mathbb{N}_0 \subseteq \mathbb{Z} \subseteq \mathbb{R} \subseteq \emptyset$ $\\$
$\emptyset \subseteq M$ und $M \subseteq M$ gilt für jede Menge

##Aussage
$A$ und $B$ Aussagen (= Aussagesätze unserer Sprache, denen genau einen Wahrheitswert $W$(wahr) oder $F$(falsch) zugeordnet werden kann)

$A \implies B$: aus $A$ folgt $B$ \\
$A \iff B$: $A$ ist äquivalent zu $B$

##Abbildung
Seien $D$ und $W$ zwei nichtleere Mengen. Unter einer Abbildung von $D$ nach $W$ versteht man eine Vorschrift $f$, die jedem $x\in D$ eindeutig ein $y \in W$ zuordnet. Man schreibt $y=f(x)$. $f(x)$ heißt das Bild von $x$ unter der Abbildung $f$. Man gibt die Abbildung an durch: $f: D \to W, x \mapsto f(x)$.
$D$ heißt Definintionsbereich, $W$ heißt Zielbereich. Die Menge $f(D)=\{f(x)|x\in D\} \subseteq W$ heißt das Bild von $f$ oder die Bildmenge von $f$. Man schreibt: $f(D)=Imf$.

###Beispiele
(1) $f:\mathbb{R} \to \mathbb{R}$ mit $f(x)=x^2$
(2) Sei $D$ eine Menge. Dann heißt die Abbildung $Id : D \to D$ mit $Id(x)=x$ für $x\in D$ die Identität von $D$. 

Seien $G$ und $H$ zwei nichtleere Mengen. \\
Dann heißt die Menge $G \times H =\{ (g,h) | g \in G,h \in H \}$ das kartesische Produkt $G$ und $H$.


##Definition
(1) Sei $G$ eine nichtleere Menge. Dann heißt eine Abbildung $\ast: G \times G \to G$ mit $(g,g') \mapsto g \ast g' \in G$ eine innere Verknüpfung auf $G$.
(2) Seien $K$ und $V$ nichtleere Mengen. Dann heißt eine Abbildung $\cdot: K \times V \to V$ mit $(\alpha, v) \mapsto \alpha \cdot v \in V$ eine äußere Verknüpfung auf $V$.

###Beispiele
(1) $+ : \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ mit $(a,b) \mapsto a + b$ und
$\cdot : \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ mit $(a,b) \mapsto a \cdot b$

sind innere Verknüpfungen auf $\mathbb{R}$
(2) $\cdot: \mathbb{N} \times \mathbb{R} \to \mathbb{R}$ mit $(n,x) \mapsto n \cdot x \in \mathbb{R}$ ist eine äußere Verknüpfung auf $\mathbb{R}$.

###Bemerkungen
(1) In $\mathbb{R}$ mit der inneren Verknüpfung + gelten die die folgenden Gesetze: $\\$
(G1) Assoziativgesetz: $(a+b)+c =a+(b+c) \\$
(G2) Es gibt ein Element $0 \in \mathbb{R}$ mit $0+a=a=a+0$ für alle $a \in \mathbb{R}$ (Existenz des neutralen Elements) $\\$
(G3) Zu jedem $a \in \mathbb{R}$ existiert ein $-a \in \mathbb{R}$ mit $a+(-a)=0$ (Existenz des inversen Elements) $\\$
(G4) Kommutativgesetz: $a+b=b+a \\$
Man sagt: $(\mathbb{R},+)$ ist eine abelsche Gruppe.

(2) Ebenso ist $\mathbb{R} \setminus {0}$ mit der Verknüpfung $\cdot$ eine abelsche Gruppe: $\\$
Assoziativgesetz und Kommutativgesetz: $\surd \\$
neutrales Element: 1 $\\$
inverses Element zu $a: \frac{1}{a}$

(3) In $\mathbb{R}$ mit den inneren Verknüpfungen $+$ und $\cdot$ gelten die Distributivgesetze: $a \cdot (b+c) = a \cdot b + a \cdot c$ und $(b+c) \cdot a = b \cdot a + c \cdot a$.

Man sagt wegen (1), (2), (3): $\mathbb{R}$ ist eine Körper. (Anderes Beispiel eines Körpers: $\mathbb{C}$)

