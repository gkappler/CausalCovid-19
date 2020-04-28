---
title: "Dateneingabe Hinterbliebene - Entwurf"
slug: data-deceased
layout: page
comments: true
---
{::options parse_block_html="true" /}

<form class="draft" method="POST" action="{{ site.staticman_data_url }}">
  <table>
  <input name="options[redirect]" type="hidden" value="https://gkappler.github.io/CausalCovid-19/">
  <!-- e.g. "2016-01-02-this-is-a-post" -->
  <input name="options[slug]" type="hidden" value="{{ page.slug }}">
  <tr><td colspan="2"><label>Nachruf<textarea name="fields[obituary]"></textarea></label></td></tr>
  {% include form_Kovariaten.md %}
  <tr><td colspan="2"><label>Erfahrungsbericht<textarea name="fields[message]"></textarea></label></td></tr>
  <tr><td><label>Sterbedatum<input name="fields[date_deceased]" type="date"></label></td>
	  <td><label>offizielle Todesursache<input name="fields[cause_of_death]" type="text"></label></td></tr>
  </table>
  <fieldset>
  <div id="reCaptcha-{{ s }}" class="g-recaptcha" data-sitekey="{{ site.reCaptcha.siteKey }}"></div>
  </fieldset>
  <button class="button" type="submit">Absenden</button>
</form>
