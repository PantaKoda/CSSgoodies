<script>
	let count = 1;

	function addDivBox() {
		const gridContainer = document.querySelector('.grid-container');
		const newBox = document.createElement('div');
		newBox.className = `box-${count}`;
		newBox.textContent = `BOX-${count}`;
		newBox.style.border = '2px solid blue';
		gridContainer?.appendChild(newBox);
		count++;
	}
</script>

<div class="grid-container"></div>
<button id="btn" on:click={addDivBox}> add div box </button>

<style>
	.grid-container {
		display: grid;
		grid-template-columns: repeat(4, 1fr);
		border: 2px solid red;
	}
</style>
