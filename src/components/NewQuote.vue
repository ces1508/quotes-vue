<template>
  <form>
    <div class=" col-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3 form-group">
      <label for="">Agrear Quote</label>
      <textarea required class="form-control" rows="3" v-model="quote"></textarea>
    </div>
    <div class="col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3 form-group">
      <button class="btn btn-primary" @click.prevent="submit">Crear</button>
    </div>
  </form>
</template>
<script>
export default {
  data () {
    return {
      quote: ''
    }
  },
  methods: {
    submit() {
      if (this.quote === '') {
        return alert('el campo no puede ser vacio')
      }
      this.$emit('submitCoute', this.quote)
      this.quote = ''
    }
  }
}
</script>
