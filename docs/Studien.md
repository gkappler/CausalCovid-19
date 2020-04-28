---
title: Studien zu Patientendaten
slug: Studien
layout: page
---
## Studien zu Patientendaten
Es gibt nur eingeschränkt Forschung auf Basis von Einzelfalldaten.
Diese Studien sind auf kleine Datensätze beschränkt.
Das hat folgende Gründe:
<ul>
	<li> Patientendaten dürfen von behandelnden Ärzt*innen nicht ohne Einverständnis weitergegeben werden.</li>
	<li> Gesundheitsbehörden führen beim Auftreten einer Seuche nur meldepflichtige Daten zusammen.
		<details markdown="details">
		<summary markdown="span">Wissen Sie, welche Informationen das genau umfasst?</summary>
		{% include comment_form.html subject="Meldepflicht" %}
		</details>
	</li>
	<li>Die Johns-Hopkins Universität stellt die Daten aus der chinesischen Provinz Hubei sowie einige Fälle mit internationalem Bezug (?) aus den USA zur Verfügung (Analysen-Repository: https://github.com/HopkinsIDD/nCoV-Sandbox).
		<details markdown="details">
		<summary markdown="span">Die Herkunft dieser Daten ist nicht transparent.</summary>
		Sind Ihnen Quellen bekannt?
		{% include comment_form.html subject="Meldepflicht" %}
		</details>
	</li>
</ul>


Sterblichkeitsraten berechnet als Anzahl von mit dem SarS-CoV-2 Erreger infizierten Verstorbenen geteilt durch die Anzahl positiv getester Meldefälle ist durch die Vorauswahl der Testpersonen in unbekanntem Maße verzerrt.
Beispielsweise werden asymptomatische Krankheitsverläufe häufiger nicht getestet als schwere Krankheitsverläufe. 
Dasselbe gilt wahrscheinlich für sehr leichte Verläufe. 
Auch gibt es Personengruppen, die keine Ärzt*in aufsuchen wollen oder können und wahrscheinlich nicht gleichmäßig über die Bevölkerung verteilt sind.

Um diese Verzerrung zu korrigieren, 
stellten Forscher die von China veröffentlichte Daten über einzelne erkrankte Patienten und weitere Daten über internationale Einzelfälle aus Internetseiten von Gesundheitsministerien und Medien zusammen.
Sie versuchten diese Verzerrungen auf Basis des Alters und Geschlechts von 3665 chinesischen Einzelfällen zu korrigieren, und schätzen für China eine Sterblichkeitsrate von 0.66%, sehr viel kleiner als auf Basis der Fallzahlen angenommene 3.67% {% cite verity_estimates_2020 %}.
Dazu verwendeten sie Korrekturverfahren, wie sie in der Epidemiologie verbreitet sind {% cite ghani_methods_2005 %}.

Zum Beispiel die Region New-York fasste Fälle aus vielen Kliniken zusammen, doch sind die Daten weder einer Analyse mit anderen Methoden zugänglich, noch können sie im Verbund mit internationalen Daten vergleichend zusammengeführt werden {% cite richardson_presenting_2020 %}.

Andere Forscher sammelten Daten aus den öffentlichen und sozialen Medien. 
Die Forscher bemängeln an ihrer eigenen Methode, dass derlei Daten durch die Eigendynamik der Medienberichterstattung verfälscht werden, die sich zudem im Laufe der Pandemie verändert {% cite sun_early_2020 %}.

[**Wenn Ihnen weitere Studien bekannt sind, fügen Sie diese bitte ein oder melden Sie diese als Kommentar in Issue #1**](https://github.com/gkappler/CausalCovid-19/issues/1).

### Literaturverzeichnis

{% bibliography --cited %}
