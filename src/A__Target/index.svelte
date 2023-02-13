<script>
export let href, target = null, alt = '', title = ''
let target__
$: target__ = target || href.split(':').length > 1 ? '_new' : '_self'
</script>

<a
	{href}
	class="A__Target {$$props.class||''}"
	target={target__}
	{...$$props}
><slot></slot></a>
