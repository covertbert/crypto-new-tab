<template lang="pug">
	section.container.ticker-section
		ticker-component
</template>

<script type="text/babel">
  import axios from 'axios'
  import TickerComponent from './TickerComponent.vue'

  export default {
    name: 'TickerSection',

    extends: {},

    props: {},

    data () {
      return {
        price: null
      }
    },

    computed: {},

    components: {TickerComponent},

    watch: {},

    methods: {},

    beforeCreate () {
    },

    mounted () {
      axios.get('https://api.cryptonator.com/api/ticker/btc-usd')
        .then((response) => {
          this.price = response.data.ticker.price
        })
        .catch((error) => {
          console.log(error)
        })
    }
  }
</script>

<style scoped lang="scss" rel="stylesheet/scss">
	.ticker-section {
		display: flex;
	}
</style>
