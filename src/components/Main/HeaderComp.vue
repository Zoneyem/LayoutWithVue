<template>
	<header class="header-container">
		
			<p><a href="">Startseite</a> > <a href=""><b>Vorteile</b></a></p>
		<h1> UNVERBINDLICHE UND KOSTENLOSE FAHRZEUGBEWERTUNG</h1>
	</header>
</template>

<script>
export default {};
</script>

<style scoped>
@media (min-width: 576px) {
	h1{
        grid-column: 2/4;
        grid-row: 2/3;
        font-size: 5px;
    }

	}

    @media (min-width: 992px) {
	main {
		grid-column: 2/5;
	}
}

header {
    display: grid;
	background-color: black;
    color: white;
    grid-column: 1/6;
    
}
a{
    color: white;
}

p{
    margin-left: 7ch;
    margin-top: 7vh;
    text-align: left;
}
h1{
    font-size: 1.9rem;
    font-weight: bold;
    text-align: center;
   align-self: center;
   justify-content: center;
    

    
}
</style>
