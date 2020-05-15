---
title: "Was alles vorstellbar ist: Wahrscheinlichkeitstheorie"
date: 2020-05-14
categories: math
layout: page
comments: true
---
<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

Besorgt frage ich mich:
Was könnte nicht alles passieren und dahinterstecken?

Die Welt ist unergründlich, 
alles hängt mit allem zusammen.
Gott ist groß.
Unsere Einsicht ist beschränkt.

Es gibt eine Mathematik des Ungewissen, die Wahrscheinlichkeitstheorie.
Sie erlaubt es, Ungewissheiten einzugrenzen und zu quantifizieren.
Sie ist die Grundlage aller wissenschaftlich informierter Entscheidungen.
Die Wahrscheinlichkeitstheorie ist die Basis aller Statistik, die
Logik aller Naturwissenschaft.
Im Wesenskern besteht sie aus nur drei Annahmen, die wir Axiome nennen, weil sie erkenntnisphilosophisch so fundamental sind, dass sie als unstrittig gelten.

**Mathematik ist ein Symbol-Gedicht**,
das fest gefügt steht,
weil es allen Zweifeln der Schlausten widerstanden hat.

Die Wahrscheinlichkeitstheorie ist die Grundlage um statistische Modelle zu quantifizieren.
Statistische Modelle sind Vereinfachungen der Wirklichkeit.
Die Vereinfachungen von Modellen bestehen in den Modellannahmen -- und diese sind genauso zweifelhaft wie kompliziert.
 
Die Wahrscheinlichkeitstheorie hilft mir sehr in der allseits ungewissen Situation der Corona-Pandemie nachzudenken darüber,

### Was alles dahinter stecken könnte?

Genau mit dieser entscheidenden Frage beginnt die Wahrscheinlichkeitstheorie!

Alles mögliche ist vorstellbar:
Ein Virus sprang von Fledermaus über Pangolin von Mensch zu Mensch. Er ist tödlich. Die Umsichtigen haben die Ausbreitung durch Maßnahmen verlangsamt.  Die Experten finden einen Impfstoff.  Milliarden werden geimpft und Ihr Leben wird gerettet.
Das ist vorstellbar.
Weil es das erste ist, was wir hören, bezeichne ich es mit dem Symbol $$\omega_1$$.

Jeder stellt sich vor was sein könnte.
Ich halte mir vor Augen, dass Sie und alle Menschen sich gerade etwas vorstellen.
Mathematik ist starrsinnig einfach und rigoros.
Es ist nicht machbar, aber denkbar, dass wir diese Vorstellungen aufzählen.
Von Reinold Becker habe ich gehört, dass manche Wirrköpfe sogar Verschwörungen vorstellbar finden!
Pfui, aber vorstellbar, also zählen wir alle $$n-1$$ sogenannten krude Verschwörungstheorien dazu $$\omega_2, \omega_3, \ldots, \omega_n$$.
Wir reden von allem Vorstellbaren:
es ist vorstellbar, dass gerade Gott mit dem Virus die Sünder dahinrafft, $$\omega_{n+1}$$, dass das Virus gar nicht existiert und alles nur ein Fehlalarm war, $$\omega_{n+2}$$. 
Trump stellt sich derzeit manchmal vor: China hat den Virus als Biowaffe entwickelt, $$\omega_{n+3}$$.
All das ist offenbar vorstellbar, weil diese Vorstellungen bedacht werden.

Die Mathematik ist nicht so arrogant, dass sie irgendeine Vorstellung von vornherein ausblendet, weil jemand findet, dass sie wirr sei.
Morgen sehen wir die Welt etwas anders, und stellen uns wieder etwas anderes vor.
Zahlloses ist Vorstellbar.
Jede mögliche Vorstellung (die Mathematik verwendet das Symbol $$\omega$$, klein omega) ist Element (symbolisch $$\in$$) einer unzählbaren Menge alles Vorstellbaren ($$\Omega$$, groß Omega):

$$
\omega \in \Omega.
$$

Es gibt Streit darüber, was $$\Omega$$ der Wahrscheinlichkeitstheorie in Wirklichkeit ist.
Paralleluniversen? Denkbare Welten? 
Im Rahmen des beweisbaren sind meine Gedanken nicht nur frei, sondern auch richtig!
Ich persönlich stelle $$\Omega$$ als die Menge alles Vorstellbaren vor, weil ich das sehr nützlich finde um über die Wirklichkeit wissenschaftlich nachzudenken ohne ein materialistischer Wissenschaftler zu sein, der ignorant einfach Möglichkeiten ausschließt.
Das darf ich ohne einen Fehler zu machen, weil es die Mathematik nicht juckt was $$\Omega$$ in Wirklichkeit ist, solange bestimmte Bedingungen erfüllt sind für die Menge $$\Omega$$ und die Teilmengen, die betrachtet werden.
Bevor wir diese Bedingungen verstehen können, betrachten wir

### Fakten

Sie fragen sich hoffentlich: Wie soll dieses Gedankenspiel zu Fakten führen?

Diese Frage nach Fakten ist leider nicht wohldefiniert:
Was ist mit "Fakten" gemeint?
Was heißt "führen"?
Wir müssen ganz genau differenzieren, welche Arten von "Fakten" es gibt, und was es alles heißen kann, "zu etwas führen".

Zum Beispiel ist ein Corona-Test-Ergebnis ein dokumentierbares Faktum, 0=negativ, 1=positiv.
Wir beginnen also mit etwas sehr einfachem: **eine Beobachtung, die dokumentiert werden kann** ist eine Art von Fakt.

Es ist auch dokumentierbar, wer oder was mit einem Corona-Test untersucht wurde.
Bei einem Test spielen also zwei Arten von Fakt eine Rolle, die wir mit unterschiedlichen Symbolen bezeichnen:
Wer untersucht wird, bezeichnen wir als $$u$$.  Welches PCRE-Testergebnis beobachtet wird, bezeichnen wir als $$x$$.

Unzählbar vieles ist vorstellbar, wie es zu einem Testergebnis kam, doch die konkrete Beobachtung $$x$$ ist immer entweder 0 oder 1, symbolisch: $$x \in  \{0, 1\}$$.
Bedenken Sie: Es ist viel vorstellbar, wieso ein positives Corona-Testergebnis $$x=1$$ für eine untersuchte $$u=$$ Papaya dokumentiert werden könnte.
Mathematisch drücken wir das so aus: es gibt Vorstellung $$\omega \in \Omega$$, die zur dokumentierten Beobachtung $$U(\omega)=$$ Papaya, und $$X(\omega)=1$$ geführt hat.
Die Klammer lese ich als "Untersuchtes U von Vorstellung klein omega war eine Papaya" und "Testergebnis X von Vorstellung klein omega war positiv".
Was von Vorstellbarem zu Fakten führt, nennt die Wahrscheinlichkeitstheorie eine Zufallsvariable.
$$U$$ und $$X$$ sind Zufallsvariablen.
Zufallsvariablen sind **mathematische Abbildungen oder Funktionen**, und man schreibt sie symbolisch

$$
\begin{align}
U & : \Omega \rightarrow \mathbb{U}\\
X & : \Omega \rightarrow \{0, 1\}
\end{align}
$$

Die Menge aller untersuchbaren Elemente bezeichnen wir symbolisch mit $$\mathbb{U}$$.  Es gibt eine ganze Menge möglicher Untersuchungsobjekte, z.B. eine ganz bestimmte Papaya $$\in \mathbb{U}$$, und Untersuchungssubjekte, z.B. Sie $$\in \mathbb{U}$$.
(In der Mathematik bezeichnen Buchstaben mit einem vertikalen Strich oft Mengen).
Wir können gerade nicht aufzählen, was alles in der Menge ist.
Wir definieren diese Menge einfach so: genau dann, wenn $$u$$ untersuchbar ist, dann ist $$u\in U$$, oder $$U = \{ u : u \text{ ist untersuchbar} \}$$ (lies: U ist die Menge aller $$u$$ für die gilt, dass $$u$$ untersuchbar ist).


### Angenommene Fakten
Ist eine Infektion mit SARS-Cov2 auch so ein Fakt?
Ja und nein:
wenn man es ganz genau nimmt, ist das sehr schwierig:
Der Corona-Virus mutiert, und jede Infektion hat einen etwas anderen Erreger.
  (Zumindest glaube ich das, weil ich gelesen habe, was RNA-Viren sind und wie Mutation funktioniert.
   Wenn ich das glaube: wieviel muss der Virus dann mutieren, bis es eine andere Infektion ist?
   Also sehr schwierig.
   Für die 5-jährige Lotta wäre sogar vorstellbar, dass unsichtbare Einhörner das Testergebnis im Labor für jene herbeizaubern, denen böse unsichtbare Geister mit einer so genannten COVID-19 Erkrankung plagen. Genau genommen ist der Kinderglaube schwer zu widerlegen...)

Ich kann die Infektion selbst nicht beobachten und dokumentieren.
Aber ich kann einen PCRE-Test $$X$$ machen, oder eine ganze Reihe von Tests, um Rückschlüsse darauf zu ziehen ob jemand infiziert ist.

Und da bin ich froh, dass ich den Medizinern vertrauen darf und muss, wenn sie von Spezifizität und Sensititivtät von Tests sprechen.
Also nehme ich an, dass es den (nicht so einfach zu dokumentierenden) Fakt gibt, ob jemand infiziert ist oder nicht.
Das ist also auch eine Zufallsvariable, $$X'$$

$$
\begin{align}
U & : \Omega \rightarrow \mathbb{U}\\
X & : \Omega \rightarrow \{0, 1\} \\
X' & : \Omega \rightarrow \{0, 1\}
\end{align}
$$

Was soll das theoretisieren?
Praktisch interessant wirds bei [Prävalenz, Sensitivität und Spezifizität](Sensitivitaet_Spezifizitaet.html)

## Wahrscheinlichkeiten und Axiome
(Entwurf)

Die Theorie befasst sich mit Ereignissen, die definiert sind als Mengen unterscheidbarer Beobachtungen.
   1. Die Wahrscheinlichkeit für ein Ereignis ist größer oder gleich Null, d.h. es gibt keine negativen Wahrscheinlichkeiten.
   2. Die Wahrscheinlichkeit, dass irgendeine aller möglichen Beobachtungen gemacht wird, ist 100%.
   3. Wenn eine (endliche) Reihe möglicher Ereignisse A,B,C,... sich gegenseitig ausschließen, so ist die Wahrscheinlichkeit, dass irgendeines der Ereignisse eintritt die Summe der Wahrscheinlichkeiten der Ereignisse.
      Zwei Ereignisse schließen sich genau dann gegenseitig aus, wenn es keine mögliche Beobachtung gibt, die beiden Ereignissen zugeordnet ist. (Und natürlich gibt es sich überschneidende Ereignisse!)
Nur soviel zur Begrifsklärung für den Laien, der Mathematik für irrelevant hält, weil falsche Modelle verwendet werden und die Wirklichkeit komplizierter ist.
