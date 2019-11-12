<template>
	<div class="container">
		<h1>Welcome to Nuxt App </h1>
		<button @click="userData()">user</button>
	</div>
</template>

<script>
	export default {
		data(){
			return{
				user:''
			}
		},
		methods:{
			async userData(){
				const ip = await this.$axios.$get('http://127.0.0.1:8000/api/me');
    			 this.user = ip;
			}
		}
	};
</script>