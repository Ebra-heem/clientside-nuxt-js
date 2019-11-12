<template>
	<div>
	   <b-navbar toggleable="lg" type="light" variant="light">
			<div class="container">
				<nuxt-link class="navbar-brand" to="/">Jwt-Auth</nuxt-link>

				    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

				    <b-collapse id="nav-collapse" is-nav>
				      <b-navbar-nav>
				        
				        <b-nav-item href="/dashboard">Dashboard</b-nav-item>
				        <b-nav-item href="/">Home</b-nav-item>
				      </b-navbar-nav>
						      <!-- Right aligned nav items -->
			     <b-navbar-nav class="ml-auto">
				      <b-nav-item href="/dashboard">Login</b-nav-item>
				        <b-nav-item href="/auth/register">Register</b-nav-item>
				  </b-navbar-nav>

				    </b-collapse>
			</div>
  	   </b-navbar>
	</div>
</template>

