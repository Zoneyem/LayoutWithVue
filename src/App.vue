<template>
	<h1>{{ title }}</h1>

	<NavbarComp />

	<MainProject />
	<FooterComp />
</template>

<script>
import * as cars from "./connect.js";
import NavbarComp from "./components/NavbarComp.vue";
import MainProject from "./components/Main/MainProject";
import FooterComp from "./components/FooterComp.vue";



export default {
	name: "App",
	data() {
		return {
			cars: cars,
			title: "Hello Boss",
		};
	},
	components: {
		NavbarComp,
		MainProject,
		FooterComp,
	},

	methods: {},
};
</script>

<style>
@import "~@fortawesome/fontawesome-free/css/all.min.css";
@import "~bootstrap/dist/css/bootstrap.min.css";

#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
	display: grid;

	margin: 0 auto;
}

@media (min-width: 576px) {
	#app {
		grid-template-columns: repeat(4, 1fr);
	}
	footer {
		grid-column: 1/5;
	}
	main {
		grid-column: 1/5;
	}

	h1 {
		grid-column: 1/5;
	}
}
@media (min-width: 992px) {
	#app {
		grid-template-columns: repeat(4, 1fr);
	}

	h1 {
		grid-column: 1/5;
	}
}
</style>
