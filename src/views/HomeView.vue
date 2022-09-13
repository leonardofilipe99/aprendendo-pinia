<template>
	<div class="home">
		<div class="count">
		{{count}}
		</div>
		<div class="button">
		<button @click="decreaseCount">-</button>
		<button @click="increaseCount">+</button>
		</div>	

		<hr>
		<div>
			Este contador esta: {{oddOrEven}}.
		</div>	
	</div>
</template>

<script setup>
import {useCounterStore} from '@/store/counter'
import {ref, computed} from 'vue'

const storeCounter = useCounterStore()
	const count = ref(0)

	const decreaseCount = () => {
		count.value--
	}

	const increaseCount = () => {
		count.value++
	}

	const oddOrEven= computed(() => {
		if (count.value % 2 ===0 ){
			return 'par'
		} else {return 'impar'}
	})
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