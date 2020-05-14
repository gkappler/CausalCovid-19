---
title: "Prävalenz, Sensitivität und Spezifizität"
date: 2020-05-14
categories: math
layout: page
---
<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
</script>
Die Definitionen der Zufallsvariablen und Symbole finden Sie im Kapitel: [Was alles vorstellbar ist: Wahrscheinlichkeitstheorie](Wahrscheinlichkeitstheorie.html)

Die Prävalenz einer Infektion ist die Wahrscheinlichkeit, dass eine Person in einer Zufallsstichprobe gerade infiziert ist (Symbolisch gesprochen $$P(X'=1)$$, wenn $$P(U)$$ eine Gleichverteilung ist). 
Das sind viele neue Wörter, über die ich später genau berichte: was ist eine "Wahrscheinlichkeit", was ist "Zufallsstichprobe" oder "Gleichverteilung"?

Aber jetzt wird es so spannend, dass ich zuerst schreibe, warum diese Wörter so interessant sind.
Ein Test ist nicht dasselbe wie die Infektion, aber er zeigt die Infektion an.
Die entscheidenden Gütekriterien eines Tests sind dabei zwei bedingte Wahrscheinlichkeiten:
- die Sensitivität $$P(X=1 \vert X'=1)$$ ist die Wahrscheinlichkeit eines positiven Testergebnisses $$X=1$$, gegeben eine Infektion $$X'=1$$, und 
- die Spezifizität $$P(X=0 \vert X'=0)$$ ist die Wahrscheinlichkeit eines negativen Testergebnisses $$X=0$$, gegeben keine Infektion $$X'=0$$.

Wenn die Prävalenz $$P(X'=1)$$ bekannt wäre, dann wäre die Wahrscheinlichkeit eines positiven Testergebnisses $$X=1$$ in einer Zufallsstichprobe 

$$
\begin{align}
P(X=1) & = P(X=1 \vert X'=1) \cdot P(X'=1) + P(X=1 \vert X'=0) \cdot P(X'=0)
\end{align}
$$

(Dieser Trick heißt Marginalisierung über bedingte Wahrscheinlichkeiten.)

Weil $$P(X=1 \vert X'=0)=1-P(X=0 \vert X'=0)$$ ist und $$P(X'=0)=1-P(X'=1)$$ ist (in der Mathematik mag man keine Prozentzahlen, 1 steht für 100%), kann man schreiben und ausmultiplizieren

$$
\begin{align}
P(X=1)
       & = sensitivity \cdot P(X'=1) + \left(1-specificity\right) \left(1-P(X'=1) \right) \\
       & = sensitivity \cdot P(X'=1) + 1-P(X'=1) - specificity + s_- P(X'=1)\\
       & = P(X'=1)\left( sensitivity - 1 + specificity \right) + 1 - specificity\\
\end{align}
$$

Die Prävalenz $$P(X'=1)$$ ist völlig unbekannt. 
Aber die Wahrscheinlichkeit eines positiven Testergebnisses $$P(X'=1)$$ können wir mit den Informationen des Robert-Koch-Instituts abschätzen:
 $$\hat{P}(X'=1)=\frac{\text{Anzahl positive Testungen}}{\text{Anzahl Testungen}}$$
(das Dach ^ steht für eine Schätzung der Wahrscheinlichkeit, die wahre Wahrscheinlichkeit ist ja unbekannt.)


Die Prävalenz können wir berechnen aus Sensitivität, Spezifizität und der geschätzten Wahrscheinlichkeit eines positiven Tests in einer Zufallsstichprobe, indem wir können die letzte Formel umformen:

$$
\begin{align}
P(X=1) - 1 + specificity      & = P(X'=1)\left( sensitivity - 1 + specificity \right)\\
P(X'=1) & = \frac{P(X=1) - 1 + specificity}{ sensitivity - 1 + specificity }
\end{align}
$$


[Eine Bayes-Schätzung der Prävalenz unter der (falschen) Annahme einer Zufallsstichprobe für die PCRE Test-Zahlen des RKI finden Sie unter diesem Link.](https://github.com/gkappler/CausalCovid-19/blob/master/PCRE.ipynb)
