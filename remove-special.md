---
layout: page
---

<div style="display: flex; flex-direction: row; width: 100%">
	<div style="width: 50%">
		<p>Original:</p>
		<textarea id="original" rows="30" style="width: 100%"></textarea>
	</div>

	<div style="width: 50%">
		<p>Sem caracteres especiais:</p>
		<textarea id="derived" rows="30" style="width: 100%"></textarea>
	</div>
</div>

<button onclick="removeSpecial();">Remove special characters</button>

<script>
	function removeSpecial() {
		const original = document.getElementById("original").value;
		const derivedElem = document.getElementById("derived");

		derivedElem.value = original.replace(/[^\P{C}\n]/gu, '');
	}
</script>