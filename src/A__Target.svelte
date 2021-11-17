<script lang="ts">
export let href:string, target:string|null|undefined = null, alt = '', title = ''
let target__:string
$: target__ = target || href.split(':').length > 1 ? '_new' : '_self'
</script>

<a
	{href}
	class="A__Target {$$props.class||''}"
	target={target__}
	{...$$props}
><slot></slot></a>
