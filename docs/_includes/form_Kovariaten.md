<tr><td colspan="2">
    <label for="female">weiblich<input type="radio" id="female" name="fields[gender]"></label>
    <label for="male">männlich<input type="radio" id="male" name="fields[gender]"></label>
</td></tr>
<tr><td><label>Testdatum<input name="fields[date_test]" type="date"></label></td>
	<td><label>Alter bei Test<input name="fields[age]" type="numeric"></label></td></tr>
<tr><td><label>Testart<input name="fields[test_type]" type="text"></label></td>
	<td>
    <label for="positive">positiv<input type="radio" id="positive" name="fields[test_result]"></label>
    <label for="negative">negativ<input type="radio" id="negative" name="fields[test_result]"></label>
</td></tr>
<tr><td><label>Gesundheitsamt Region<input name="fields[date_test]" type="text"></label></td>
<td><label>Gesundheitsamt E-Mail<input name="fields[doctor]" type="email"></label></td></tr>
<tr><td colspan="2">Vorerkrankungen:
          {%- for v in site.data.Vorerkrankungen -%}
		    <label for="{{ v.id }}">{{ v.name }}</label>
            <input type="checkbox" id="{{ v.id }}">
          {%- endfor -%}
		  <br/>
	<label>Sonstige Vorerkrankungen<input name="fields[preconditions]" type="text"></label></td></tr>
<tr><td colspan="2"><label>Symptome<input name="fields[symptoms]" type="text"></label></td></tr>
<tr><td><label>Beginn der Erkrankung<input name="fields[disease_onset]" type="date"></label></td>
	<td><label>Hospitalisierung<input name="fields[date_hospital]" type="date"></label></td></tr>
<tr><td colspan="2"><label>Interventionen<input name="fields[interventions]" type="text"></label></td></tr>
