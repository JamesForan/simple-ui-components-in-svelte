<input type="text" autocomplete="off"
	{id}
	{name}
	{title}
	{placeholder}
	bind:value="{value}"
	on:keydown="{onkeydown}"
	on:change="{onchange}">
<script>
export let value = '';
export let id = undefined;
export let name = undefined;
export let title = undefined;
export let placeholder = undefined;

const DECIMAL_SEPARATOR = '.';
const allowedKeys = [
	'0',
	'1',
	'2',
	'3',
	'4',
	'5',
	'6',
	'7',
	'8',
	'9',
	'ArrowLeft',
	'ArrowDown',
	'ArrowUp',
	'ArrowRight',
	'Backspace',
	'Delete',
	'Tab',
	'Meta',
];

function onkeydown (e) {
	if (allowedKeys.includes(e.key)) return;
	if (e.key === DECIMAL_SEPARATOR && !value.includes(DECIMAL_SEPARATOR)) return;
	e.preventDefault();
}

function onchange () {
	const num = parseFloat(value);
	value = isNaN(num) ? '' : num;
}
</script>
