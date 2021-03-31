<template>
	<section>
		<h2>{{greeting}}, {{name}}!</h2>
		<slot>デフォルトスロット</slot>
	</section>
</template>

<script>
	module.exports = {
		props: {
			name: {
				type: String,
				default: 'World',
				required: false
			}
		},
		data: function () {
			return {
				greeting: 'Hello'
			}
		}
	}
</script>

<style>
	section {
		border: 2px dashed seagreen;
		margin: 60px 30px;
		padding: 30px;
	}
	h2 {
		color: seagreen;
		margin-bottom: 20px;
		text-align: center;
	}
	p {
		margin-bottom: 10px;
	}
	.orange {
		color: orange;
		font-weight: bold;
	}
</style>