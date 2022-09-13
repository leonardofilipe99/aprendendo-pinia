<template>
	<div class="home">
		<Counter />
		
		<div class="button">
		<button @click="storeCounter.decreaseCount">-</button>
		<button @click="storeCounter.increaseCount">+</button>
		</div>	

		<hr>
		<div>
			Este contador esta: {{storeCounter.oddOrEven}}.
		</div>

		<hr>
		<div>
			<br>
			<h3>Editar contador</h3>
			<input 
			v-model="storeCounter.count"
			type="number" 
			>
		</div>	
	</div>
</template>

<script setup>
import {useCounterStore} from '@/stores/counter'
import Counter from '@/components/Counter.vue'
const storeCounter = useCounterStore()

</script>

<style>
	.count {
		font-size: 60px;
		margin:20px;
	}

	.button button{
		font-size: 40px;
		margin: 10px;
	}
</style>