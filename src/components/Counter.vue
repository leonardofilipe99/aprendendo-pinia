<template>
		<div class="count">
		{{storeCounter.count}} 
		</div>
</template>

<script setup>
import {useCounterStore} from '@/stores/counter'
import {ref, computed} from 'vue'

const storeCounter = useCounterStore()

</script>