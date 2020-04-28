---
title: Ursache-Wirkung
slug: Kausalitaetstheorie
layout: page
---
<script type="text/javascript" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

Eine Veröffentlichung von Falldaten würde eine diverse Forschungsarbeiten mit unterschiedlichen statistischen Verfahren ermöglichen.
Ich selbst forschte im Bereich kausaler Inferenzstatistik und bin mit meinen Kollegen überzeugt, dass diese Methoden in der heutigen Situation helfen können, entscheidende, aber noch immer offene Fragen für die Allgemeinheit, Politiker und Wissenschaftler zu klären.
Im folgenden versuche ich, aus dieser theoretischen Perspektive Möglichkeiten zur Analyse und den Bedarf an Daten allgemeinverständlich darzustellen.

## Wie viele Menschen sterben an Covid-19? Übersterblichkeit und Kausalität
Die Kausalitätstheorie nach Rolf Steyer beginnt mit einer formalen Klärung von... Begriffen durch ein Zufallsexperiment.
Zur verständlichen Beschreibung der Theorie in Bezug auf Covid-19 die reduzierteste Fassung ohne Berücksichtigung der Zeitpunkte oder des Krankheitsverlaufs:
- Zur Testung wird eine Person $$U=u$$ aus der Population ausgewählt (nicht randomisiert, sondern gemäß Testprotokoll).
- Das Testergebnis der Person wird erhoben, $$X=x$$. 
- Kovariaten werden erhoben $$Z=z$$ (Alter, Geschlecht und Vorerkrankungen etc..)
 <!-- - Erkrankt die Person ($$S=1$$) oder bleibt sie asymptomatisch ($$S=0$$) -->
- Ist die Person verstorben ($$Y=0$$) oder ist sie genesen ($$Y=1$$)?

Wahrscheinlichkeitstheoretisch sind dies Zufallsvariablen
$$
\begin{align}
U & : \Omega \rightarrow \text{Population}\\
X & : \Omega \rightarrow {0,1}\\
Z & : \Omega \rightarrow Z_{1} \times...\times Z_{n}\\
% <!-- - S & : \Omega \rightarrow {0,1} -->
Y & : \Omega \rightarrow {0,1}
\end{align}
$$
### Teststichprobe und Population
Die Testung und die Auswahl der Stichprobe liefert keine direkte Einschätzung, wieviele Personen in der Bevölkerung wirklich infiziert sind. 
Dazu müssten im obigen Zufallsexperiment die Verteilung der Probanden $$U$$ durch eine randomisierte/repräsentative Auswahl $$U'$$ ersetzt werden.
- Eine Person $$U'=u$$ wird gleichverteilt aus der Population ausgewählt (also zufällig = randomisiert; annäherungsweise wird in der Praxis zuweilen aus test-ökonomischen Gründen eine [geschichtete Zufallsstichprobe (Wikipedia)](https://de.wikipedia.org/wiki/Geschichtete_Zufallsstichprobe) erhoben).
- Die Person ist mit Covid-19 infiziert, $$X'$$ (kann nicht direkt beobachtet werden, sondern nur anhand von Tests). 

### Infektion und Test
Die Infektion mit SARS-Cov2 ist eine nicht direkt beobachtbare Zufallsvariable $$X'$$, und kann nur indirekt durch Tests erhoben werden.
Tests sind niemals absolut zuverlässig sondern durch Sensititivtät und Spezifizität ([Wikipedia](https://de.wikipedia.org/wiki/Beurteilung_eines_bin%C3%A4ren_Klassifikators#Sensitivit%C3%A4t_und_Falsch-negativ-Rate)) gekennzeichnet, in bedingten Wahrscheinlichkeiten ausgedrückt (siehe [Serology-based tests for COVID-19](https://www.centerforhealthsecurity.org/resources/COVID-19/serology/Serology-based-tests-for-COVID-19.html)):
- Sensitivität bezeichnet die Wahrscheinlichkeit, dass eine infizierte Person auch positiv getestet wird, $$P(X=1 \vert X'=1)$$
- Spezifizität bezeichnet die Wahrscheinlichkeit, dass eine nicht infizierte Person auch negativ getestet wird, $$P(X=0 \vert X'=0)$$

### Was ist die Übersterblichkeit durch Corona in der erhobenen Stichprobe?
Die Anteile (Wahrscheinlichkeiten) der versterbenden Personen
- wenn test-negativ: $$P(Y=0 \vert X=0)$$,
- wenn test-positiv: $$P(Y=0 \vert X=1)$$.

Der durchschnittliche kausale Effekt einer Covid-19-Erkrankung auf die Sterblichkeit innerhalb der getesteten Stichprobe entspricht der Differenz dieser Wahrscheinlichkeiten $$P(Y=0 \vert X=1)-P(Y=0 \vert X=0)$$ und kann als durch *Covid-19 bedingte Übersterblichkeit innerhalb der Stichprobe* interpretiert werden.

Hier stellen sich grundsätzliche Probleme:
- Die Stichprobe ist nicht repräsentativ für die Gesamtbevölkerung.
- Es ist anhand der erfassten Testdaten nicht mögich, die Wahrscheinlichkeit zu messen, dass eine Person mit negativem Test verstirbt. Diese Wahrscheinlichkeit könnte jedoch auf Basis veröffentlichter Sterberaten der Vorjahre abgeschätzt werden.
- Die Zufallsvariablen der Genesung $$Y$$ kann erst nach dem Ende der Erkrankung erhoben werden. 
  <!-- Wahrscheinlichkeit mit positivem Test zu versterben ist nur für den Anteil der positiv getesteten zu ermitteln, die bereits genesen oder verstorben sind. -->

Für Personen, die durch Geschlecht, Alter und Vorerkrankungen $$Z=z$$ charakterisiert sind, und 
- positiv auf Covid19 getestet wurden, ist das bedingte Sterberisiko $$P(Y=0 \vert Z=z,X=1)$$,
- negativ auf Covid19 getestet wurden, ist das bedingte Sterberisiko $$P(Y=0 \vert Z=z,X=0)$$,
Der $$Z$$-bedingte durchschnittliche kausale Effekt von Covid19 auf die Sterberate ist definiert als die Differenz dieser bedingten Wahrscheinlichkeiten: $$ACE_{Z=z}(Y \vert X) = P(Y=0 \vert Z=z,X=1) - P(Y=0 \vert Z=z,X=0)$$.
Dieser bedingte durchschnittliche Effekt $$ACE_{Z=z}(Y \vert X)$$ is spezifisch für Personen, die durch Kovariaten $$Z=z$$ (Alter, Vorerkrankungen, etc.) charakterisiert sind, und für diese Gruppe definiert als der Mehr-Anteil der versterbenden Personen, die Covid-19-positiv getestet wurden, über die zu erwartende Sterblichkeitsrate von Covid-19-negativ getesteten Personen hinaus.
*Es handelt sich also um die Covid-19 bedingte Übersterblichkeit von Personen mit Kovariaten Z=z.* 

### Verallgemeinerung auf die Bevölkerung
#### Durchschnittliche kausale Effekte
Es ist möglich, die durchschnittlichen kausalen Effekte in der Gesamtbevölkerung zu berechnen, wenn die $$Z *$$-bedingte kausale Regression* $$E_{Z=z}(Y \vert X)$$ kausal erwartungstreu und die Verteilung der Kovariaten in der Gesamtbevölkerung,  $$P'(Z=z)$$,  bekannt ist ($$P'(Z)$$ kann von der Verteilung $$P(Z)$$ in der getesteten Stichprobe abweichen! Dies ist insbesondere der Fall, wenn nur symptomatische Patienten in Krankenhäusern getestet werden.).

Die zu erwartende durchschnittliche Mortalitätsrate von Covid-19 in der Gesamtbevölkerung entspricht dann dem durchschnittlichen kausalen Effekt $$ACE(Y \vert X) = \sum_{z \in Z(\Omega)} P'(Z=z) ACE_{Z=z}(Y \vert X)$$.

Es ist mathematisch beweisbar, dass Marginalisierung über $$P'(Z=z)$$ eine erwartungstreue Schätzung des durchschnittlichen kausalen Effekts ergibt, wenn die Bedingung erfüllt ist, dass $$E_{Z=z}(Y \vert X)$$ kausal erwartungstreu ist für alle $$z \in Z(\Omega)$$.

#### Kausale Erwartungstreue 
Definitionen
1. Der ($$Z=z$$) *-bedingte kausal erwartungstreue Erwartungswert* von $$Y$$ gegeben $$X=x$$ ist definiert als

   $$CUE_{Z=z}(Y \vert X=x) = \sum_u E_{Z=z}(Y \vert U=u,X=x)P_{Z=z}(U=u)$$.
2. Die $$Z$$ *-bedingte kausale Regression* $$E_{Z=z}(Y \vert X)$$ ist kausal erwartungstreu, wenn für alle $$Z=z$$

   $$E(Y \vert Z=z, X=x)$$ = CUE_{Z=z}(Y \vert X=x).

Es ist beweisbar, dass $$E_{Z=z}(Y \vert X)$$ kausal erwartungstreu ist, wenn mindestens eine der folgenden Bedingungen erfüllt ist:
1. Die Überlebenswahrscheinlichkeit $$E(Y \vert X, U, Z)$$, bedingt auf Person $$U$$ mit Testung $$X$$ und Kovariaten $$Z$$, ist fast sicher (d.h. für alle Kovariaten $$Z=z$$ mit $$P(Z=z)>0$$) gleich der Überlebenswahrscheinlichkeit $$E(Y \vert X, Z)$$, bedingt auf Testung $$X$$ und Kovariaten $$Z$$.

   Dies ist *erfüllt, wenn* $$Z$$ *all jene Kovariaten umfasst, welche Genesungs-/Sterbewahrscheinlichkeit einer Person beeinflussen.*

   Daher ist eine umfangreiche Erfassung und Veröffentlichung aller Risiko- und Protektivfaktoren der Erkrankten notwendig.

2. Positive Testung $$X$$ und Auswahlwahrscheinlichkeit $$U$$ sind stochastisch unabhängig gegeben $$Z$$. 

   Das Ziel der selektiven Testung durch Kontaktnachverfolgung ist, die Infizierten mit größerer wahrscheinlicher zu testen als die wahrscheinlich nicht Infizierten.  Wenn dieses Ziel erreicht wird, ist diese Bedingung *nicht erfüllt*.

3. Personen-Infektions-Homogenität $$E(Y \vert X,U)$$ = E(Y \vert X) ist gegeben.

   Dies ist *nicht erfüllt*, da offenbar nicht alle test-positiven Personen die gleichen Wahrscheinlichkeiten zu genesen und zu versterben haben.
Nur die erste dieser Bedingungen ist erfüllbar, wenn aufgrund der Testkapazitäten nicht randomisiert getestet wird (2.).
Daher ist es nötig, umfangreiche Patientendaten zur Verfügung zu stellen.

Auf Basis einer repräsentativen Erhebung von Antikörpern scheint Bedingung 2. erfüllt, und eine Einschränkung der Personendaten auf bestimmte Fragestellungen wie Alter, Geschlecht, bestimmte Vorerkrankungen ist hinreichend.
Jedoch selbst in diesem Fall ist es vorteilhaft, möglichst umfangreiche Patientendaten zu veröffentlichen, um Kovariaten zu identifizieren, die einen Einfluss auf den Verlauf der Erkrankung haben, obwohl dies a-priori nicht vorhergesehen wurde.

Steyer, R., Nachtigall, C., Wüthrich-Martone, O., & Kraus, K. (2002). Causal regression models III: Covariates, conditional, and unconditional average causal effects. Methods of Psychological Research Online, 7(1), 41–68.


### Anmerkungen zur Erweiterung des Zufallsexperiments:
- $$X$$: Berücksichtigung verschiedener Tests
- Berücksichtigungen der Zeitpunkte von Testungen, ggf. des Krankheitsverlaufs. 
- $$Y$$: Vielleicht mit Zeitintervall der Genesung 2 Wochen, vielleicht mehrwertig: genesen, hospitalisiert, verstorben.

### Statistische Modellierung
Kausale Inferenzstatistik selbst ist kein statistisches Modell.
Vielmehr formuliert kausale Inferenzstatistik die abstrakte wahrscheinlichkeitstheoretische Frage, wie kausale Effekte allgemein definiert sind, auch für nicht-randomisierte kontrollierte Studien.
Statistische Modelle werden in einem zweiten Schritt verwendet, um die Wahrscheinlichkeiten an Covid-19 zu versterben, bedingt auf Kovariaten und Teststatus in Regressionen zu schätzen.
In diesem zweiten Schritt haben Forscher statistische Modelle zu testen und kritisch auszuwählen, um zu erwartungstreuen Vorhersagen und Abschätzungen ihrer Zuverlässigkeit zu gelangen.

<!-- Dieses sei an einem sehr einfachen Modell illustriert, um den Altersgruppen-bedingten kausalen Effekt von Covid-19 auf die Sterblichkeit zu schätzen. -->
<!-- So kann die Covid-19 bedingte Übersterblichkeit für jede Altergruppe geschätzt werden. -->

<!-- Die hierfür benötigten Daten seien aufbereitet wie in folgender Tabelle: -->
<!-- \vert i \vert Fall          \vert A: Alter, Jahre \vert X: Covid-19 Test \vert Y: genesen \vert verstorben   \vert -->
<!-- \vert---+---------------+-----------------+------------------+------------+--------------\vert -->
<!-- \vert 1 \vert verstorben    \vert              72 \vert                1 \vert          0 \vert            1 \vert -->
<!-- \vert 2 \vert genesen       \vert              75 \vert                1 \vert          1 \vert            0 \vert -->
<!-- \vert 3 \vert noch erkrankt \vert              65 \vert                1 \vert          0 \vert            0 \vert -->
<!-- \vert   \vert ...           \vert                 \vert                  \vert            \vert              \vert -->
<!-- \vert n \vert               \vert                 \vert                  \vert            \vert              \vert -->
<!-- (Anmerkung: 0=nein, 1=ja, Fett: Abkürzung in Formeln im Folgenden) -->
<!-- Solange positive Testfälle noch erkrankt sind, werden sie im Modell nicht berücksichtigt. -->

<!-- Zähle in jeder Altersdekade $$I_{d}(a)=\left\{\begin{array}{ll}1 & \text{falls }  10 d\le a<10 (d+1)\\ 0 & \text{sonst}\end{array}$$: -->
<!--   - die Verstorbenen $$N^V_{d}=\sum_{i=1}^n I_{d}(a_i)V_i$$, -->
<!--   - die Genesenen $$N^G_{d}=\sum_{i=1}^n I_{d}(a_i)G_i$$. -->
<!-- Damit kann die Wahrscheinlichkeit -->
<!-- $$P(Y=0 \vert Z=z, X=1) \approx \hat{P}(Y=0 \vert Z=z, X=1) = \frac{}{}$$, -->

<!-- Es ist fraglich ob Daten für Covid-19 negative Fälle entsprechend erfasst werden könnten: -->
<!-- \vert Fall             \vert Alter \vert Test \vert verstorben \vert genesen \vert -->
<!-- \vert------------------+-------+------+------------+---------\vert -->
<!-- \vert 1, noch erkrankt \vert    62 \vert    0 \vert          0 \vert       0 \vert -->
<!-- \vert 2, verstorben    \vert    82 \vert    0 \vert          1 \vert       0 \vert -->
<!-- \vert 3, genesen       \vert    35 \vert    0 \vert          0 \vert       0 \vert -->
<!-- \vert ...              \vert       \vert      \vert            \vert         \vert -->
<!-- (Anmerkung: genesen ist hier konstant 0=nein) -->
<!-- Selbst wenn diese Daten zur Verfügung stehen, ist die Frage der Sterblichkeit kritisch: -->
<!-- Zeitpunkt, Erfassung und Zuordnung  die Personen , wann  -->

<!-- Die Modellierung demonstriert auch eine Möglichkeit, fehlenden Daten zur Sterblichkeit Fälle auszugleichen. -->




Logistische Regressionen
1. Modelle logit $$P(Y=0 \vert Z_{i}, X) = \alpha_{0} + \alpha_{1} X + \beta Z_{i} + \gamma X Z_{i}$$ für alle Kovariaten $$Z_{i}$$.
2. Haupteffekte und Interaktionseffekte mit $$X$$: logit $$P(Y=0 \vert Z, X) = \alpha_{0} + \alpha_{1} X + \sum_{i} \beta_{i} Z_{i}  + \sum_{i} \gamma_{i} X Z_{i}$$.
3. Komplexere Modelle zur Abschätzung sind denkbar und wünschenswert.  Ich schlage vor, dass diese Daten anonymisiert öffentlich gemacht werden sollten, um die Grundlage für einen freien Wettbewerb für die Vorhersage der Mortalität aus den Kovariaten zu ermöglichen.
4. Bei den voraussichtlich großen Fallzahlen ist ggf. eine nonparametrische und modellfreie Vorhersage möglich.


### Falls Daten fehlen
Voraussichtlich sind manche dieser Daten nicht für alle getesteten Personen verfügbar.
In diesem Fall kann mit geeigneten Verteilungsannahmen die Datenlücke ausgeglichen werden.

Falls die Vorerkrankungen Test-negativer Personen nicht verfügbar sind, ist ggf. eine akzeptable Annahme, dass die Vorerkrankungen der Getesteten ebenso verteilt sind wie in der Gesamtpopulation, bedingt auf das Alter.

Da Sterbedaten der negativ getesteten nicht verfügbar sein dürften, könnte ihre Sterberate anhand publizierter Mortalitäten der Vorerkrankungen und des Alters pro Jahr abgeschätzt werden.

## Wann hilft und wann schadet Intubation als medizinische Maßnahme?  

Diese Frage beginnt erneut mit der formalen Begriffsklärung durch das Zufallsexperiment.
- Zur Testung wird eine SARS-CoV2 positive Person $$U=u$$ in Intensivpflege ausgewählt
- Die Sauerstoffsättigung im Blut wird erhoben, $$O=o$$.
- Kovariaten werden erhoben $$Z=z$$ (Alter, Geschlecht und Vorerkrankungen etc..).
- Wird die Person intubiert ($$X=1$$) oder wird sie nicht intubiert ($$X=0$$)
- Ist die Person verstorben ($$Y=0$$) oder ist sie genesen ($$Y=1$$)?

Der bedingte kausale Effekt der Intubation auf die Genesungswahrscheinlichkeit für Patienten mit $$Z=z, O=o$$ ist
$$ACE_{Z=z,O=o}(Y \vert X) = P(Y=1 \vert X=1, Z=z, O=o)-P(Y=1 \vert X=0, Z=z, O=o)$$.

