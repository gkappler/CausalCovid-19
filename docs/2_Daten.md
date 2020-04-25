---
title: Daten
slug: Daten
layout: page
---

Leider werden derzeit nur zusammengefasste Fallzahlen systematisch veröffentlicht, mit unterschiedlicher Aufschlüsselung nach Land, Geschlecht, und Alter.
Auf Basis dieser Fallzahlen, d.h. ohne Daten auf Ebene von Einzelfällen lassen sich jedoch obige drängendsten Fragen nicht beantworten.


Es liegen bisher leider wenige [Studien zu Daten auf der Ebene von Einzelfällen](2.2_Studien.html) der Covid-19 Erkrankung vor.
Diese Studien verwenden Daten, welche zum Teil mühsam von den Forschern aus den Sozialen Medien und oft ungenannten Quellen zusammengestellt wurden.
Die meines Wissens umfangreichste Datensammlung der Johns-Hopkins Universität stellt zusammengeführte Daten als [Daten-Exploration](https://docs.google.com/spreadsheets/d/1jS24DjSPVWa4iuxuD4OAXrE3QeI8c9BC1hSlqr-NMiU/edit#gid=1841943470][google Tabelle]] zur Verfügung. Die darin enthaltenen Datenspalten sind in der [[Case-Data Exploration.ipynb) aufgelistet.
**Wenn Ihnen weitere Datensätze bekannt sind, informieren Sie mich bitte als Kommentar in [Issue #2](https://github.com/gkappler/CausalCovid-19/issues/2).**


Daten auf Ebene von Einzelfällen sind erforderlich zur bestmöglichen Erforschung der Gefährlichkeit der Erkrankung und der Wirksamkeit von medizinischen Maßnahmen.
Sie fehlen aber, bzw. werden für einzelne Studien jeweils aus den Krankenhausdaten zusammengestellt und nicht öffentlich geteilt.



# Benötigte Daten
Optimalerweise würden für die Berechnungen folgende anonymisierten Daten zu jedem getesteten Mitbürger verwendet:
- Testdatum Test-Art und Testergebnis
- Vorerkrankungen
- Hospitalisierungsdatum, falls hospitalisiert
- Entlassungsdatum, falls entlassen
- Versterbedatum, falls verstorben
- Obduktionsdaten, falls verfügbar
- Alter, Geschlecht, wenn möglich Lebensumstände (Rauchen, Luftqualität, Stadt, Land, Ernährungsgewohnheiten, etc)

Zur Bestimmung der kausalen Effekte medizinischer Maßnahmen werden zudem benötigt:
- durchgeführte medizinische Maßnahmen (Intubation, Medikamente)

## Optionen zur Datensammlung

### Gesundheitsämter, Krankenhäuser, Ärzte
Sind an strenge Datenschutzverordnungen gebunden und können die erforderlichen Daten aus rechtlichen Gründen nicht zur Verfügung stellen?


### Angehörige tragen Ihre Daten in einem Formular ein.
Sie haben alle Rechte an allen Ihren persönlichen Gesundheitsdaten.
Wir wollen alle das Gute tun, und Leben retten.  Am besten können Sie das mit Ihren anonymen Daten tun.
**Haben die Hinterbliebenen das Recht, die Daten Ihrer verstorbenen Angehörigen mit einem Nachruf zu veröffentlichen?**

Anhand der mail-Adresse von behandelndem Arzt/Krankenhaus könnten die eingegebenen Daten verifiziert werden.

Entwurf:
  
  <form method="POST" action="{{ site.staticman_data_url }}">
  <table>
  <tr><td><input name="options[redirect]" type="hidden" value="https://gkappler.github.io/CausalCovid-19/"></td></tr>
  <!-- e.g. "2016-01-02-this-is-a-post" -->
  <tr><td><input name="options[slug]" type="hidden" value="{{ page.slug }}"></td></tr>
  <tr><td><label>Testdatum<input name="fields[date_test]" type="date"></label></td></tr>
  <tr><td><label>Testart(?) und Testergebnis<input name="fields[test_result]" type="text"></label></td></tr>
  <tr><td><label>Geschlecht<input name="fields[gender]" type="numeric"></label></td></tr>
  <tr><td><label>Alter bei Test<input name="fields[age]" type="numeric"></label></td></tr>
  <tr><td><label>Erkrankung<input name="fields[disease_onset]" type="date"></label></td></tr>
  <tr><td><label>Symptome<input name="fields[symptoms]" type="text"></label></td></tr>
  <tr><td><label>behandelnder Arzt<input name="fields[doctor]" type="email"></label></td></tr>
  <tr><td><label>Hospitalisierung<input name="fields[date_hospital]" type="date"></label></td></tr>
  <tr><td><label>Interventionen<input name="fields[interventions]" type="text"></label></td></tr>
  <tr><td><label>Genesung<input name="fields[date_recovered]" type="date"></label></td></tr>
  <tr><td><label>Sterbedatum<input name="fields[date_deceased]" type="date"></label></td></tr>
  <tr><td><label>offizielle Todesursache<input name="fields[cause_of_death]" type="text"></label></td></tr>
  <tr><td><label>Erfahrungsbericht<textarea name="fields[message]"></textarea></label></td></tr>
  <tr><td><label>Nachruf<textarea name="fields[obituary]"></textarea></label></td></tr>
  
  <tr><td><button type="submit">Absenden!</button></td></tr>
  </table>
  </form>


## Falls Daten fehlen
Voraussichtlich sind manche dieser Daten nicht für alle getesteten Personen verfügbar.
In diesem Fall kann mit geeigneten Verteilungsannahmen die Datenlücke ausgeglichen werden.

Zur statistischen Schätzung dieser Größen sind von den Gesundheitsbehörden folgende Daten erfolderlich:
- Anonymisierte Daten aller getesteten Personen (Testergebnis /X=x/ und Kovariaten /Z=z/).
- Verteilung /P(Z=z)/ in der Population.
- Genesen/Versterben /Y=y/.

Falls die Vorerkrankungen nicht Test-negativer Personen nicht verfügbar sind, ist ggf. eine akzeptable Annahme, dass die Vorerkrankungen der Getesteten ebenso verteilt sind wie in der Gesamtpopulation, bedingt auf das Alter.

Da Sterbedaten der negativ getesteten nicht verfügbar sein dürften, könnte ihre Sterberate /P(Y=0 | Z=z,X=0)/ anhand publizierter Mortalitäten der Vorerkrankungen und des Alters pro Jahr abgeschätzt werden.
Selbst wenn diese Sterberaten verfügbar wäre, ist zu klären, ob es nicht aussagekräftiger ist, die Sterberate innerhalb eines Jahres zugrundezulegen.
