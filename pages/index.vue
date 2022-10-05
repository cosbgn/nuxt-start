<template>
	<div>
		Without Trailing slash:
		<ul>
			<li><a href="https://rx-gamma.vercel.app">https://rx-gamma.vercel.app</a> Works</li>
			<li><a href="https://rx-gamma.vercel.app?foo=bar">https://rx-gamma.vercel.app?foo=bar</a> Works</li>
			<li style="color:red;"><a href="https://rx-gamma.vercel.app?foo=bar+x">https://rx-gamma.vercel.app?foo=bar+x</a> Doesn't Work</li>
		</ul>

		With Trailing slash:
		<ul>
			<li><a href="https://rx-gamma.vercel.app/">https://rx-gamma.vercel.app/</a> Works</li>
			<li><a href="https://rx-gamma.vercel.app/?foo=bar">https://rx-gamma.vercel.app/?foo=bar</a> Works</li>
			<li style="color:red;"><a href="https://rx-gamma.vercel.app/?foo=bar+x">https://rx-gamma.vercel.app/?foo=bar+x</a> Doesn't Work</li>
		</ul>

		<p> The issue is in the + sign (I think)</p>
	</div>
</template>