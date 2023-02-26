<template>
	<ul>
		<li>消息编号：{{id}}</li>
		<li>消息标题：{{title}}</li>
		<!-- <li>{{a}}-{{b}}-{{c}}-{{d}}</li> -->
	</ul>
</template>

<script>
	export default {
		name:'Detail',
        // props:['a', 'b', 'c', 'd'],
		props:['id','title'],
		mounted() {
			// console.log(this.$route)
		},
	}
</script>