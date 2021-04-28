<script>
	let count = 0;

	const handleClick = () => {
		count += 1;
	};
	// log the value of count whenever it changes:
	$: console.log(`the count is ${count}`);

	// reactive statements
	$: if (count >= 10) {
		alert(`count is dangerously high!`);
		count = 9;
	}
</script>

<button on:click={handleClick}>
	clicked
	{count}
	{count == 1 ? 'time' : 'times'}
</button>
