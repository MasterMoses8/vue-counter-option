<!-- 
  options api 
  option api requires a default object to be exported.
  be aware of the syntax required.
-->
<script>
	export default {
		// create data object to define accessible variables
		data() {
			return {
				// create variable count default value of 0
				count: 0,
			};
		},

		// array of methods and functions to be called / used
		methods: {
			// create add function to increase count
			addToCount() {
				// when called identify the exisiting variable for count and increment by 1
				this.count++;
			},

			// create subtract function to decrease count
			subtractFromCount() {
				// when called, identify the existing variable for count and decrease by 1
				this.count--;
			},
		},
	};
</script>

<!-- javascript template to render the html for the page -->
<template>
	<main>
		<div>
			<h4>The current count is...</h4>
			<!-- access value of count state object -->
			<h1>{{ count }}</h1>
			<!-- button calls on click listener to use subtrack function -->
			<button @click="subtractFromCount">-</button>
			<!-- button calls on click listener to use add function -->
			<button @click="addToCount">+</button>
		</div>
	</main>
</template>

<!-- scoped style will affect only this component -->
<style scoped>
	main {
		height: 100vh;
		width: 100vw;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	div {
		text-align: center;
	}
</style>
