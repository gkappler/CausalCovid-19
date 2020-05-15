---
title: Schätzungen der Prävalenz in der Teststichprobe
date: 2020-05-15
layout: post
categories: pcre
comments: true
redirect_from:
---
Die Meldezahlen von Infektionen mit SARS-Cov2 sind abhängig von der Zahl durchgeführter Testungen.  Zudem dominieren bei geringeren tatsächlichen Infektionszahlen zunehmend falsch-positive Testungen die berichteten Zahlen.
Der Anteil wirklich infizierter Personen in der Teststichprobe (Prävalenz) ist die relevantere Größe und kann geschätzt werden auf Basis der Anzahl von Testungen, der Zahl Test-Positiver und unter Annahme der bekannten Spezifizität=89% und Sensitivität=94% des SARS-Cov2 PCR Tests. 

Basis der Analysen sind die Daten des [RKI Situationsberichts 2020-05-13](https://www.rki.de/DE/Content/InfAZ/N/Neuartiges_Coronavirus/Situationsberichte/2020-05-13-de.pdf?__blob=publicationFile).
Punktschätzer wurden anhand von Formeln berechnet, welche die [Prävalenz aus Sensitivität und Spezifizität und der Wahrscheinlichkeit positiver Testung](https://gkappler.github.io/CausalCovid-19/Sensitivitaet_Spezifizitaet.html) herleiten.
Zudem wurde die Prävalenz Bayes-inferenzstatistisch mit einem Binomialmodell geschätzt. Bayes-Modelle ermöglichen besonders robuste Schätzungen auch bei kleinen Stichproben bzw. wenigen Test-positiven Fällen.
[Die Posterior-Verteilungen der so geschätzen Prävalenz in der Teststrichprobe von Wochen <10 bis 19 werden berichtet.](https://github.com/gkappler/CausalCovid-19/blob/master/PCRE.ipynb)

**Diese Ergebnisse wurden noch nicht von Fachkollegen gegengeprüft. Wenn Sie die Methoden begutachten können, wäre ich Ihnen über kritische Rückmeldung sehr dankbar!**

In Woche 5 ergibt sich unter den 408'348 Testungen eine erwartete Zahl tatsächlich infizierter Personen von 14'922,9 Personen (vgl. mit 36'885 positiven Testungen).
In Woche 19 ergibt sich unter den 382'154 Testungen eine erwartete Zahl tatsächlich infizierter Personen von 2,3 Personen (vgl. mit 10'187 positiven Testungen).

Einschränkend ist zu sagen:
- Infektionen treten in Clustern auf. Das verwendete Modell geht aber von einer einzigen Stichprobe aus.
  **Die Testungdaten auf Landkreisebene sollten analysiert werden**.
- Sensitivität und Spezifizität müssen anhand der Quelle validiert werden. Ggf. sollten diese Parameter selbst als Zufallsvariablen mit einem informierten Prior verwendet werden.
