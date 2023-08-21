<template>
	<nav>
		<div class="container">
			<router-link to="/">Home</router-link> |
			<router-link to="/about">About</router-link>
		</div>
	</nav>
	<main>
		<div class="container">
			<router-view />
		</div>
	</main>
</template>

<style lang="scss">
@import 'styles/style.scss'
</style>
