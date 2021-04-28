<script>
	let numbers = [1, 2, 3, 4];

	function addNumber() {
		// Assignments to properties of arrays and objects
		numbers[numbers.length] = numbers.length + 1;

		/*
		** Or use:
			numbers.push(numbers.length + 1);
			//   redundant assignment to update the result of applying array methods
			numbers = numbers;
		*/

		/*
		** Or use:
		// Spread Operator
			numbers = [...numbers, numbers.length + 1];

		*/
	}
	$: sum = numbers.reduce((t, n) => t + n, 0);
</script>

<p>{numbers.join(' + ')} = {sum}</p>

<button on:click={addNumber}> Add a number </button>
