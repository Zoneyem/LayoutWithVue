<template>
	<footer class="footer-container">
		<footer class="bg-light text-center text-lg-start">
			<!-- Copyright -->
			<div class="text-center p-3" style="background-color: rgba(0, 0, 0, 0.2)">
				<ul>
					<li
						><a href="mailto:leonel.zone@yahoo.fr"
							>E-Mail:leonel.zone@yahoo.fr</a
						></li
					>
					<li><a href="tel:+499123456789">Tel:+491771577232</a></li>
					<li><a href="">Impressum</a></li>
					<li><a href="">Adresse</a></li>
				</ul>
			</div>
			<!-- Copyright -->
		</footer>
	</footer>
</template>

<script>
export default {};
</script>

<style scoped>
@media (min-width: 576px) {
	nav {
		grid-column: 1/5;
	}
}
@media (min-width: 992px) {
	nav {
		grid-column: 1/5;
	}
}
footer {
	display: block;
}

ul {
	display: flex;
	justify-content: space-between;
}

li {
	display: inline;
}
a{
    text-decoration: none;
}
</style>
