<template>
  <div>
    <h3>hay {{ count }}</h3>
    <div class="progress">
      <div class="progress-bar" role="progressbar" :style={{ width=getPercentaje }} :aria-valuenow="getPercentage" aria-valuemin="0" aria-valuemax="100"></div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    count: Number
  },
  computed: {
    getPercentage () {
      console.log(this.count * 10)
      return this.count * 10
    }
  }
}
</script>

