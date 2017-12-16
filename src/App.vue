<template lang="pug">
	#app
		ticker-section
	</div>
</template>

<script>
  import TickerSection from './components/ticker/TickerSection.vue'

  export default {
    name: 'app',
    components: {
      TickerSection
    }
  }
</script>

<style lang="scss" rel="stylesheet/scss">
	html {
		font-size: 16px;

		@media screen and (min-width: 900px) {
			font-size: 18px;
		}

		@media screen and (min-width: 1200px) {
			font-size: 20px;
		}
	}

	#app {
		font-family: 'Avenir', Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #2c3e50;
		margin-top: 60px;
	}
</style>
