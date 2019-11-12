<template>
	<div class="container">
		<div class="col-md-6 offset-md-3">
			<div class="card mt-4">
				<div class="card-header">
					<p>Register</p>
				</div>
				<div class="card-body">
					<form @submit.prevent="register">
						<div class="form-group">
							<label for="name"> Name</label>
							<input v-model="form.name" type="text" class="form-control" placeholder="Name">
						</div>
						<div class="form-group">
							<label for="name"> Email</label>
							<input v-model="form.email" type="text" class="form-control" placeholder="Email">
						</div>
						<div class="form-group">
							<label for="name"> Password</label>
							<input v-model="form.password" type="password" class="form-control" placeholder="Password">
						</div>
						<div class="form-group">
							
							<input type="submit" class="btn btn-success w-100" value="Register">
						</div>
					</form>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
	export default{
		data(){
			return{
				form:{
					name:'',
					email:'',
					password:''
				}
			}
		},
		methods:{
			async register(){
			try {
		   		 await this.$axios.$post('/auth/register', this.form);
			} catch(e) {
		    	return;
			}

				this.$auth.login({data: this.form});

				this.$router.push({name:'index'});
			}
		}
	}
</script>