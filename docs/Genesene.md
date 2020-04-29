---
title: "Dateneingabe Genesene - Entwurf"
slug: data-recovered
layout: page
comments: true
---
{::options parse_block_html="true" /}

Bitte stellen Sie Ihre gesundheitlichen Daten anonym und öffentlich zur Verfügung:

Bitte schreiben Sie uns Ihre Erlebnisse, Gedanken und Gefühle:
<form class="draft" method="POST" action="{{ site.staticman_data_url }}">
  <table>
  <input name="options[redirect]" type="hidden" value="https://gkappler.github.io/CausalCovid-19/">
  <tr><td colspan="2">
	<label>Erfahrungsbericht<textarea name="fields[message]"></textarea></label>
  </td></tr>
  <!-- e.g. "2016-01-02-this-is-a-post" -->
  <input name="options[slug]" type="hidden" value="{{ page.slug }}">
  {% include form_Kovariaten.md %}
  <tr><td colspan="2"><label>Genesung am<input name="fields[date_recovered]" type="date"></label></td></tr>
  </table>
  <fieldset>
  <div id="reCaptcha-{{ s }}" class="g-recaptcha" data-sitekey="{{ site.reCaptcha.siteKey }}"></div>
  </fieldset>
  <button class="button" type="submit">Absenden</button>
</form>
