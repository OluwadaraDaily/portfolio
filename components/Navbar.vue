<template>
    <div class="main__header">
        <header class="header">
			<div class="logo">
				<i class="fas fa-archway fa-2x"></i>
                <font-awesome-icon :icon="['fas', 'archway']"></font-awesome-icon>
			</div>
			<nav class="nav">
				<ul class="nav__items">
					<li class="nav__link"><nuxt-link to="/">Home</nuxt-link></li>
					<li class="nav__link"><nuxt-link to="#projects">Projects</nuxt-link></li>
					<li class="nav__link"><a href="https://oluwadaradaily.hashnode.dev/" target="__blank">Blog</a></li>
					<li class="nav__link"><nuxt-link to="#interests">Interests</nuxt-link></li>
					<li class="nav__link"><nuxt-link to="#contact-me">Contact Me</nuxt-link></li>
				</ul>
			</nav>
		</header>
    </div>    
</template>

<script>
export default {
    name: "Navbar"
}
</script>

<style scoped>
    @import url('../assets/css/navbar.scss');
</style>