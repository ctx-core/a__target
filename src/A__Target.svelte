<script lang="ts">
export let href:string
export let target:string|null|undefined = null
export let alt = ''
export let title = ''
let target__
$: target__ = target || href.split(':').length > 1 ? '_new' : '_self'
</script>

<a
	{href}
	class="A__Target {$$props.class||''}"
	target={target__}
	{...$$props}
><slot></slot></a>
