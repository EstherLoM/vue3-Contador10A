<script>

export default {
	data: () => ({
		contador:500,
		ventana:false,
	}),
	methods: {
	 incrementar(){
	 this.contador++;
	 },
	 disminuir(){
	 this.contador--;
	 },
	 resetear(){
	 this.contador=10;
	 },
	}
};
</script>

<template> 
    <div class="container">
   
		<img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
	    <small>
		<h1>Hola desde VUE.js 3</h1>
		</small>
		<h2>Contador {{ contador }}</h2>

		<button @click="incrementar()"> Sumar uno</button>
		<button @click="disminuir()">Restar uno</button>
		<button @click="resetear()">Reiniciar</button><br>

    </div>

	<button @click.prevente="ventana=true"> Abrir</button>

   <div v-bind="ventana" v-if="ventana">

   <b>Nombre:</b><i>Lopez Muñoz Esther</i><br>
   <b>Materia:</b><i>Desarrollo Movil Integral</i><br>
   <b>Profesor:</b><i>Hector Bernardo Ortega Gines</i><br>
   <b><i>10mo A - DGS</i></b><br>
   <button @click.prevente="ventana=false"> Cerrar</button>
   </div>
</template>

<style scoped>

.container{
	text-align: center;
	}
	
	h1{
	color: Blue;
	font-weight:bolder;
	}

	h2{
	font-size:2.5rem;
	}
	
	
	button{
	cursor: pointer;
	font-size: 1.5rem;
	margin: 0px 8px;
	}
	
	small{
	color: #666;
	}
	

</style>
