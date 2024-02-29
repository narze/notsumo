<script lang="ts">
	const mapping = {
		ข: 'ひ',
		ค: 'の',
		ง: 'ゝ',
		จ: 'ヌ',
		น: 'は',
		ด: 'の',
		ต: 'め',
		ท: 'れ',
		ม: 'み',
		ย: 'も',
		บ: 'ひ',
		อ: 'ゆ',
		ณ: 'ぬ',
		ร: 'ち',
		ล: 'ス',
		ส: 'ス',
		ว: 'つ',
		ห: 'カ゚',
		ะ: 'ニ',
                เ: 'エ',
		แ: 'い',
		า: 'ク',
		ไ: 'て',
		โ: 'イ',
		ๆ: 'ウ',
	};

	let input = $state('ใครรวย');
	let output = $derived.by(() => {
		return input
			.split('')
			.map((th) => {
				return mapping[th] || th;
			})
			.join('');
	});
</script>

<center><h1>のつも</h1></center>

<!-- svelte-ignore a11y-autofocus -->
<textarea bind:value={input} rows="5" autofocus></textarea>
<textarea readonly rows="5">{output}</textarea>

<footer>
	<a href="https://github.com/narze/notsumo">Github</a>
</footer>

<style>
	textarea {
		text-align: center;
	}
</style>
