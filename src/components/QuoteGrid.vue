<template>
  <div class="row">
    <qoute @click.native="deleteQuote(index)" v-for="(quote, index) in quotes" :key="index" >
      {{ quote }}
    </qoute>
  </div>
</template>
<script>
import Quoute from './Quote.vue'
export default {
  props: {
    quotes: Array
  },
  components: {
    'qoute': Quoute
  },
  methods: {
    deleteQuote (index) {
      this.$emit('quoteToDelete', index)
    }
  }
}
</script>
<style>

</style>

