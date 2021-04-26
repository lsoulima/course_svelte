<script>
	let string = `this string contains some <strong>HTML!!!</strong>`;
</script>

<!-- Show Text with tags -->
<p>{string}</p>

<!-- Use the special {@html ...} tag, to interpret HTML code -->
<p>
	{@html string}
</p>
