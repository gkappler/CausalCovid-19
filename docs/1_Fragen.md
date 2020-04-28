---
title: "Forschungsfragen"
slug: Fragen
layout: page
comments: yes
---
{::options parse_block_html="true" /}
<details><summary markdown="span">Wie hoch ist Ihr persönliches Risiko, falls Sie mit SarS-CoV2 infiziert sind?</summary>
Es ist Gegenstand der Diskussion, in welchem Ausmaß Menschen "an" oder "mit" Covid-19 versterben.
Die Frage ist, ob Corona *ursächlich* war für das Versterben einer Person, oder ob die Person nicht in einem überschaubaren Zeitraum ohnehin gestorben wäre. 
Damit zusammen hängen die Fragen, wie gefährlich Covid-19 im Vergleich zu beispielsweise Influenza ist, und für welche Personengruppen sie besonders gefährlich ist.
Diese Fragen sind relevant, um die Wirksamkeit und Verhältnismäßigkeit möglicher Maßnahmen zu diskutieren.

Anhand der veröffentlichten Infektions- und Sterblichkeitszahlen sind diese Fragen nicht zu beantworten.
Antikörpertests auf einer representativ ausgewählten Gruppe von Menschen können die Frage der durchschnittlichen Sterblichkeit statistisch klären, und es gibt Hinweise, dass die Bevölkerung bereits stärker immunisiert sein könnte als befürchtet {% cite bendavid_covid-19_2020 braun_presence_2020 %}. 
Wie hoch das Risiko für Personen mit bestimmten Vorerkrankungen ist, wird derzeit auf Grundlage des Expertenwissens durch das Urteil des begutachtenden Pathologen durch Obduktionen geklärt.
Die Übersterblichkeitsstatistik ([EUROMOMO](https://www.euromomo.eu/)) fasst die Folgen der Covid-19 Erkrankung und aller lokal getroffenen Maßnahmen ununterscheidbar zusammen.
Beispielsweise lassen sich anhand der Übersterblichkeit Maßnahmen nicht bewerten, die in Italien möglicherweise zu einer hohen Zahl vermeidbarer Krankenhausinfektionen führten {% cite boccia_what_2020 %}.
</details>


<details><summary markdown="span">Wann hilft und wann schadet Intubation?</summary>
Die Ärzt\*innen in den Intensivstationen müssen täglich Behandlungsentscheidungen treffen. Sie treffen diese aufgrund ihrer Erfahrung mit anderen Lungenerkrankungen. Es gibt allerdings zahlreiche Berichte, dass Covid-19 sich bedeutend von anderen Krankkeiten unterscheidet. Der Austausch von Ärzt\*innen untereinander findet derzeit statt, aber nicht in systematischer, technisch unterstützter Weise.
Beispielsweise traten einige Ärzt\*innen in Europa und den USA an die Öffentlichkeit, und berichteten über Ihre Erfahrungen mit dem Intubieren bei an Covid-19 erkrankten Patienten:
Sie äußerten sich überrascht, dass selbst bei niedriger Sauerstoffsättigung von ca. 50% viele ihrer Patienten ohne Intubation die Krankheit überstehen, jedoch die intubierten Patienten zumeist versterben
([New York Times Artikel](https://www.nytimes.com/2020/04/14/nyregion/new-york-coronavirus.html){:target="_blank"},
[New York Times @ YouTube](https://www.youtube.com/watch?v=bp5RMutCNoI){:target="_blank"}).
</details>

<details><summary markdown="span">Welche antiviralen Medikamente helfen wem?</summary>
Ärzte lernen von den Beobachtungen während ihrer Arbeit und - in einer neuen Pandemie - durch Versuch, Irrtum und Erfolg.
Diese Erfahrungen können randomisierte Studien zur Wirksamkeit der Intubationsbehandlung anregen.
Aber der übliche kontrollierte Forschungsprozess braucht Zeit und erfodert unter anderem sorgfältig ethische Abwägungen, wer in der Experimentalgruppe behandelt wird, und wer nicht (vgl. Drosten).
Heute gibt es diese wissenschaftlichen, randomisierten Studien zum Behandlungserfolg von Interventionen noch nicht
In dieser katastrophalen Situation ist es besonders wichtig, nicht nur Erfahrungsberichte zu teilen oder auf kontrollierte Studien zu warten. 
Bis dahin könnten Informationen über Interventionen und deren Erfolg systematisch mit einer Datenspende erkrankter Personen gesammelt werden, um so wissenschaftliche Einschätzungen zu erhalten.
</details>


## Statistische Analysen von Ursache und Wirkung
Kann man wissenschaftlich über Ursachen und Wirkungen forschen und sprechen, auch wenn kontrollierte Experimente noch nicht vorliegen?
Dies ist nicht unmöglich!
Es gibt statistische Verfahren der kausalen Inferenzstatistik, um *ohne* randomisierte Studien zu schätzen, welche medizinischen Maßnahmen Heilung ursächlich begünstigen bzw. negativ beeinflussen:
Die Theorie kausaler Effekte {% cite steyer_causal_2000 steyer_causal_2000-1 steyer_causal_2002 %} und propensity-score Methoden {% cite rosenbaum_central_1983 %}.

Vereinfacht gesagt systematisieren diese Verfahren die Analyse von beobachteten Erfahrungen und korrigieren mathematisch die Verzerrungen, welche bei nicht-randomisierten Beobachtungen unvermeidlich sind.

Diese Verfahren wurden für Umstände wie die Covid-19-Pandemie entwickelt, um kausale Effekte in Beobachtungsstudien zu schätzen, d.h. wenn es nicht möglich ist, wie bei einem kontrollieren Experiment eine Kontroll- und Experimentalgruppe zu bilden.
 <!-- erlaubt es auf Basis nicht experimentell und randomisiert erhobener Daten ursächliche Effekte zu schätzen.Sie  -->
 <!-- , beispielsweise aus ethischen oder ökonomischen Gründen. -->
Zur Schätzung von kausalen Inferenz-Modellen wäre es erforderlich, in Krankenhäusern und Gesundheitsämtern vorliegende Daten auf der Ebene von Einzelfällen zu erheben und anonymisiert der Forschung zur Verfügung zu stellen.

<details><summary markdown="span">Diese Verfahren ermöglichen mit hinreichender Daten evidenz-basierte Schätzungen, um...</summary>
1. die **Wirksamkeit medizinischer Maßnahmen** durch systematische Beobachtung und Erfassung zu bestimmen.
2. eine dringend benötigte Schätzung der **durchschnittlichen Mortalität** von Covid-19 bezogen auf die Gesamtbevölkerung zu berechnen.
3. das **bedingte Risiko**, im Falle einer Infektion zu versterben, verlässlich zu quantifizieren, für Personen eines bestimmten **Alters, Geschlechts** und auch für Personen mit **bestimmten bekannten Vorerkrankungen**.
4. die Folgen von Plänen abzuschätzen, einen hinlänglich großen Teil der Bevölkerung **natürlich zu immunisieren** und um dadurch eine Ausbreitung der Krankheit wesentlich zu vermindern (Herdenimmunisierung): 

   Dafür wäre die Frage zu beantworten, welche 60%-70% der Bevölkerung mit dem geringsten Risiko eines schweren Krankheitsverlaufs erkranken könnten, und wie groß das Risiko dieser Personengruppen wäre, an der Erkrankung zu versterben.
5. diese zu erwartenden Folgen einer kontrollierten Herdenimmunisierung den erwarteten Folgen anderer Maßnahmen, zum Beispiel des Risikos von Nebenwirkungen eines in begrenztem Umfang getesteten Impfstoffs, gegenüberzustellen.

</details>
Diese Fragen sind in der gegenwärtigen Situation von höchster Dringlichkeit, um behandelnden Ärzt\*innen, Bürger\*innen sowie Politiker*innen eine verlässlichere, öffentlich nachvollziehbare Grundlage für ihre Entscheidungen zu geben.


### Literaturverzeichnis

{% bibliography --cited %}
