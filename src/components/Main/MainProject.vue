<template>
	<main class="container-wrapper">
		<HeaderComp />
		<OpelComp test="c'est un test" />
		<!--je passe le props ici, ensuite de l'anreigistre en string dans le component en question et puis je le reutilise comme data property-->
	<!--
			<OpelComp>
			<h1>Me voici</h1>
			<p 
				>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit optio
				sit voluptatibus sapiente adipisci aspernatur tenetur quas cupiditate
				totam corporis.</p
			>
		</OpelComp>
	-->
	</main>
</template>

<script>
import HeaderComp from "./HeaderComp.vue";
import OpelComp from "./OpelComp.vue";
export default {
	data() {
		return {
			autos: [
				{
					name: "zone",
					surname: "leonel",
				},
				{
					name: "Dicka",
					surname: "claudine",
				},
			],
		};
	},

	components: {
		HeaderComp,
		OpelComp,
	},
};
</script>

<style>
@media (min-width: 576px) {
	main {
		grid-template-columns: repeat(4, 1fr);
		grid-column: 1/5;
	}
}

@media (min-width: 992px) {
	main {
		grid-template-columns: repeat(4, 1fr);
		grid-column: 1/5;
	}
}

main {
	background: white;

	display: grid;
	grid-template-columns: repeat(5, 1fr);
	grid-auto-rows: minmax(20ch, auto);
	gap: 10px;
}

div {
	background: white;
}

.premier {
	padding: 70px 0;
	border: 3px solid green;
	text-align: center;

	grid-column: 1/6;
}

p {
	text-align: left;
	justify-content: flex-start;
}

img {
	width: 100%;
	height: auto;
}
</style>
