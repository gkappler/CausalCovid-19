---
title: Datenspende
slug: data-collection
layout: page
---
{::options parse_block_html="true" /}
Gesundheitsämter, Krankenhäuser, Ärzt\*innen
sind an strenge Datenschutzverordnungen gebunden und können die erforderlichen Daten aus rechtlichen Gründen nicht zur Verfügung stellen.

Jeder hat das Recht, seine persönlichen Gesundheitsdaten zur Verfügung zu stellen.
Die Erfahrung der letzten Wochen hat gezeigt, dass die Mehrheit der Menschen dabei helfen möchte, Leben zu retten und die Pandemie so wirksam wie möglich zu bekämpfen, und dabei auch zu erheblichen Opfern bereit ist.
Als Erkrankter können sie das in besonders wirksamer Weise mit einer anonymen einmaligen Spende Ihrer Erkrankungsdaten tun.

<details><summary markdown="span">**Wie funktioniert die Erkrankungs-Datenspende?**</summary>
1. Anonyme Datenerfassung:
   Ihre Gesundheitsdaten sind sehr privat, und daher ist es entscheidend, Ihre Identität zu schützen.
2. Öffentliche Daten für die internationale Öffentlichkeit:
   - Ihr anonymer Datensatz wird im Datenarchiv nach Absendung mit einer Creative-Commons Lizenz veröffentlicht.
   - Der aktuellste Datenstand kann von der Wissenschaftsgemeinde beforscht werden. 
3. Prüfung der Datenqualität durch behandelnde Ärzt\*innen und Kliniken.
   - Bei der Datenerfassung wird die email des meldenden Gesundheitsamtes erfragt.
   - Das Gesundheitsamt kann anhand des Datums von Test, Aufnahme und Entlassung/Tod die behandelnde Ärzt\*in ermitteln. 
   - Die behandelnde Ärzt\*in kann Ihre Angaben mit Patientenakten abgleichen und auf Korrektheit bestätigen.
</details>

### Zur Dateneingabe
<a class="button" href="Genesene.html" style="display: block;">
	Sind Sie von einer Covid-19-Erkrankung genesen?
</a>
<a class="button" href="Angehoerige.html" style="display: block;">
   Haben Sie einen Angehörigen mit einer Covid-19-Erkrankung verloren?
</a>
<a class="button" href="Nichterkrankte.html" style="display: block;">
   Können Sie uns mitteilen, wie Sie **indirekt** von der Corona-Pandemie betroffen sind?
</a>


# Benötigte Daten
Derzeit werden nur zusammengefasste Fallzahlen systematisch veröffentlicht, mit unterschiedlicher Aufschlüsselung nach Land, Geschlecht und Alter.
Auf Basis dieser Fallzahlen, d.h. ohne Daten auf Ebene von Einzelfällen, lassen sich jedoch [wichtige ursächliche Fragen](Kausalitaet.html) nicht zuverlässig beantworten.
Daten auf Ebene von Einzelfällen sind erforderlich zur bestmöglichen Erforschung der Gefährlichkeit der Erkrankung und der Wirksamkeit von medizinischen Maßnahmen.

<details><summary markdown="span">Gibt es keine wissenschaftlichen Studien mit Einzelfalldaten?</summary>
Es liegen bisher erst wenige [Studien zu Daten auf der Ebene von Einzelfällen](Studien.html) der Covid-19-Erkrankung vor.
Diese Studien sind auf vergleichsweise kleine Datensätze beschränkt, 
die je Studie aus den Krankenhausdaten zusammengestellt und nicht öffentlich geteilt werden.
In einigen Fällen wurden Daten mühsam von den Forschern aus Sozialen Medien und oft ungenannten Quellen zusammengestellt.
Das hat möglicherweise folgende Gründe:
<ul>
	<li>Patientendaten dürfen von behandelnden Ärzten nicht ohne Einverständnis weitergegeben werden.</li>
	<li>Gesundheitsbehörden führen im Seuchenfall nur meldepflichtige Daten zusammen.
	
		
		<details markdown="details">
		<summary markdown="span">Wissen Sie welche Informationen das genau umfasst?</summary>
		{% include comment_form.html subject="Meldepflicht" %}
		</details>
	</li>
	<li>Die Johns-Hopkins Universität stellt die Daten aus Hubei Province, China, sowie einige internationale Fälle aus den USA zur Verfügung (<a href="https://github.com/HopkinsIDD/nCoV-Sandbox">John Hopkins-Analysen-Repository</a>).
		Diese umfangreichste Datensammlung stellt zusammengeführte Daten als <a href="https://docs.google.com/spreadsheets/d/1jS24DjSPVWa4iuxuD4OAXrE3QeI8c9BC1hSlqr-NMiU/edit#gid=1841943470">Google Tabelle</a> zur Verfügung. 
		Die darin enthaltenen Datenspalten sind in der <a href="https://github.com/gkappler/CausalCovid-19/blob/master/Case-Data%20Exploration.ipynb">Case-Data Exploration.ipynb</a> aufgelistet.
		
		<a href="https://github.com/gkappler/CausalCovid-19/issues/2">Wenn Ihnen weitere Datensätze bekannt sind, weisen Sie bitte in Issue #2 darauf hin.</a>

		<details markdown="details">
		<summary markdown="span">Die Herkunft dieser Daten ist nicht transparent.</summary>
		Wissen Sie Quellen?
		{% include comment_form.html subject="data-source" %}
		</details>
	</li>
</ul>
</details>

Eine erwartungstreue Schätzung kausaler Effekte ist möglich, wenn all jene Kovariaten erfasst werden, welche Genesungs-/Sterbewahrscheinlichkeit einer Person mit beeinflussen (vgl. [Kausalitätstheorie](Kausalitaetsmodell.html#kausale-erwartungstreue)).
Daher ist eine umfangreiche Erfassung und Veröffentlichung aller Risiko- und Protektivfaktoren der Erkrankten notwendig.

Optimalerweise stünden für die Forschung folgende anonymisierten Daten zu jeder getesteten Person zur Verfügung:
- Testdatum Test-Art und Testergebnis
- Vorerkrankungen
- Hospitalisierungsdatum, falls hospitalisiert
- Entlassungsdatum, falls entlassen
- Versterbedatum, falls verstorben
- Obduktionsdaten, falls verfügbar
- Alter, Geschlecht, wenn möglich Lebensumstände (Rauchen, Luftqualität, Stadt, Land, Ernährungsgewohnheiten, etc)
- möglicher Ursache/Ort der Ansteckung, z.B. Familienkreis, Arbeitsstelle, öffentliche Verkehrsmittel, Geschäft, Gastronomie, Menschenansammlung?
- Behandelnder Arzt/Klinik

Zur Untersuchung, welche medizinischen Maßnahmen werden zudem benötigt:
- durchgeführte medizinische Maßnahmen (Intubation, Medikamente)
- Diagnostische Daten

<details class="question"><summary markdown="span">Sind Sie Ärzt\*in/medizinischer Experte?</summary>
- Welche diagnostischen Kennwerte und klinischen Maßnahmen sollten ausdrücklich erfragt werden?
- Unter welchen Umständen würden Sie eine Erkrankungs-Datenspende aktiv oder auf Nachfrage empfehlen?
<div markdown="0">
	{% include comment_form.html subject="doctor" %}
</div>
</details>


<details class="question"><summary markdown="span">Sind Sie an SarS-CoV-2 Erforschung interessierter Wissenschaftler?</summary>
- Bräuchten Sie weitere Daten für Ihre Forschung?
- Unter welchen Umständen würden Sie eine Erkrankungs-Datenspende aktiv oder auf Nachfrage empfehlen?
<div markdown="0">
	{% include comment_form.html subject="researcher" %}
</div>
</details>



