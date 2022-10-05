<template>
	<div>
		Without Trailing slash:
		<ul>
			<li><a :href="url">{{url}}</a> Works</li>
			<li><a :href="`${url}?foo=bar`">{{url}}?foo=bar</a> Works</li>
			<li style="color:red;"><a :href="`${url}?foo=bar+x`">{{url}}?foo=bar+x</a> Doesn't Work</li>
		</ul>

		With Trailing slash:
		<ul>
			<li><a :href="`${url}/`">{{url}}/</a> Works</li>
			<li><a :href="`${url}/?foo=bar`">{{url}}/?foo=bar</a> Works</li>
			<li style="color:red;"><a :href="`${url}/?foo=bar+x`">{{url}}/?foo=bar+x</a> Doesn't Work</li>
		</ul>

		<p> The issue is in the + sign (I think)</p>
	</div>
</template>
<script setup>
	const url = computed(() => window?.location?.origin ?? '')
</script>