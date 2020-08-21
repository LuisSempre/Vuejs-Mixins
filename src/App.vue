<template>
	<div id="app">
		<h1>Filtros & Mixins (Desafio)</h1>
		<p>{{ frase | espacoPorVirgula }}</p>

		<p>{{ frase | contarPalavras }}</p>

		<p>{{ fraseComVirgulas }}</p>
		<p>{{ fraseComTamanhos }}</p>
	</div>
</template>

<script>
import fraseMixin from './fraseMixin';

export default {
	mixins: [
		fraseMixin
	],
	data () {
		return {
			frase: 'Essa é a frase usada nos desafios.'
		}
	},
	filters: {
		espacoPorVirgula(valor){
			return valor.replace(/ /g, ',')
		}
	},


}
</script>

<style>
#app {
	font-family: 'Avenir', Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
	font-size: 2.5rem;
}
</style>
