<template>
<div>{{test}}</div>
	<p>
		SIE ERHALTEN EINE KOSTENLOSE UND UNVERBINDLICHE FAHRZEUGBEWERTUNG FÜR IHR
		AUTO IN EURO EINSCHLIESSLICH MWST. DIESE BASIERT AUF DER GRUNDLAGE VON
		MARKTBEOBACHTUNGEN, JÜNGSTEN TRANSAKTIONEN VON VERGLEICHSFAHRZEUGEN UND
		IHREN INFORMATIONEN ZUM ZUSTAND DES FAHRZEUGS.
	</p>
	<div class="section-wrapper">
		<section class="opel-section" v-for="car in cars" :key="car.id">
			<p class="short-text"
				><b>{{ car.kurz }} </b>
			</p>
			<img :src="car.url" alt="" />
			<p class="opel-text">
				<span>{{ car.desc }}</span></p
			>
		</section>
	</div>

	
</template>

<script>
export default {
	props: ['test'],
	data() {
		return {
			cars: [
				{
					url: "https://i.imgur.com/AApgSCD.gif",
					kurz: "EINFACH",
					desc: "            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Harum omnis fugit quas, pariatur explicabo deleniti. Dolorem ipsam ducimus deleniti tempore quia nam hic debitis odit eius? Quam sit id natus ducimus nam fugiat pariatur tenetur!",
				},
				{
					url: "https://i.imgur.com/MvJTKSI.gif",
					kurz: "SCHNELL",
					desc: "            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Harum omnis fugit quas, pariatur explicabo deleniti. Dolorem ipsam ducimus deleniti tempore quia nam hic debitis odit eius? Quam sit id natus ducimus nam fugiat pariatur tenetur!",
				},
				{
					url: "https://i.imgur.com/IHE6opI.gif",
					kurz: "SICHER",
					desc: "            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Harum omnis fugit quas, pariatur explicabo deleniti. Dolorem ipsam ducimus deleniti tempore quia nam hic debitis odit eius? Quam sit id natus ducimus nam fugiat pariatur tenetur!",
				},
			],
		};
	},
};
</script>

<style scoped>
@media (min-width: 576px) {
	.section-wrapper {
		grid-template-columns: repeat(4, 1fr);
		grid-column: 2/5;
	}

	.opel-section {
		grid-column: 2/5;
	}
	.opel-text {
		text-align: center;
	}
}

@media (min-width: 576px) {
}

@media (min-width: 992px) {
	.section-wrapper {
		grid-column: 2/5;
		gap: 10px;
		display: flex;
	}
	.opel-section {
		grid-column: 2/5;
	}
}

p {
	grid-column: 1/6;
	color: black;
	font-weight: bolder;
	font-size: 1.5rem;
	margin-top: 10ch;
	text-align: center;
	font-family: "Times New Roman", Times, serif;
}

.opel-text {
	font-style: normal;
	text-align: left;
	font-family: "Times New Roman", Times, serif;

	font-weight: 20;
}

.short-text {
	text-align: center;
}
</style>
