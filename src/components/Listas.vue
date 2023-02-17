<script>
	import ElementoLi from './li.vue';
	import ElementoJson from '../assets/data.json';


	export default {
		data() {
			emits: ['check']


			return {
				listas: ElementoJson,
				counter: 0

			};

		},
		components: {
			ElementoLi
		},

		methods:{

		}

	}


</script>



<template>
	<section v-for="etapa in listas.componentes" class="border-solid border-2 rounded-lg border-current mb-6 ml-6 mr-6"
		:archivoUno='etapa'>
		<div>
			<h2 class="font-bold text-xl text-center">
				Sección {{etapa.id}}:
				{{etapa.nombre}}
			</h2>

		</div>
		<div class="justify-start ml-3 mb-5">
			<ul>
				<ElementoLi v-for="etapaDos in etapa.pasos" :archivo='etapaDos'> </ElementoLi>

			</ul>
			<div class="bg-gray-200 h-1 mb-4 ml-2 mr-2 mt-4">
				<div class="bg-blue-600 h-1 mr-4" style="width: 50%"></div>
			</div>
		</div>


	</section>
	
	

</template>