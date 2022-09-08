<script>
	export let sport = [
		{ label: ''},
		{ label: ''},
		{ label: ''}
	];
	
	let selectioner = sport[1];
</script>


{#each sport as value}
	<label>
		<input
			type="radio"
			bind:group={selectioner}
			name="amount"
			value={value}
		> {value.label}
	</label>
{/each}

{selectioner.label}