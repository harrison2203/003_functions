
<script setup>
import { ref } from 'vue';

const inputAmount = ref();
const inputPercentage = ref();
const total = ref();
const showResult = ref(false);

function tips() {
  total.value = inputAmount.value * (inputPercentage.value / 100);
  showResult.value = true;
}
</script>

<template>

<div class="bg-sky-100 pb-8">
	<h1 class="text-center text-4xl letter-spacing: -0.05em font-bold pt-6">Calculer un pourcentage</h1>
</div>

<div class="w-full max-w-sm p-4 bg-white border border-gray-200 rounded-lg shadow sm:p-6 md:p-8 dark:bg-gray-800 dark:border-gray-700">
    <form class="space-y-6" action="#">
        <h5 class="text-xl font-medium text-gray-900 dark:text-white">Tips</h5>
        
        <div>
            <label for="amount-input" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Amount:</label>
            <input id="amount-input" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white" 
            v-model="inputAmount"
			/>
        </div>

        <div>
            <label for="percentage-input" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Percentage</label>
            <input id="percentage-input" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white" required
            v-model="inputPercentage"
			/>
        </div>

		<div>
            <label for="total" class="block mb-2 text-sm font-medium text-gray-900 dark:text-white">Total:</label>
            <input id="total" class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white" required
            v-model="total"
			/>
        </div>

        <button type="button" class="w-full text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
		@click="tips"
		>Click
		</button>
    </form>
</div>

  </template>


<style>

</style>