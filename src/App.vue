<template>
  <div id="app" class='container'>
    <Header :count="quotes.length" />
    <add-qoute @submitCoute="addQoute" />
    <list-quotes :quotes="quotes" @quoteToDelete="deleteQuote"/>
    <div class="row">
      <div class="col-sm-12 text-center">
        <div class="alert alert-info">
          para eliminar alguno, dar click sobre el
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import ListQoutes from './components/QuoteGrid.vue'
import AddQoute from './components/NewQuote.vue'
import Header from './components/Header.vue'

export default {
  components: {
    "list-quotes": ListQoutes,
    'addQoute': AddQoute,
    'Header': Header
  },
  data () {
    return {
      quotes: ['soy un quote'],
      maxQuotes: 10
    }
  },
  methods: {
    addQoute (quote) {
      if (this.quotes.length === 10) {
        return alert('no puedes agregar mas, lo sentimos')
      }
      this.quotes.push(quote)
    },
    deleteQuote (index) {
      this.quotes.splice(index, 1)
    }
  }
}
</script>

