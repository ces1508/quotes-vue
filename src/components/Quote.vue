<template>
  <div class="col-sm-6 col-md-4 col-lg-3">
    <div class="panel panel-default">
      <div class="panel-body qoute">
        <slot></slot>
      </div>
    </div>
  </div>
</template>
<script>
export default {

}
</script>
<style scoped>
  .panel-body {
    font-family: 'Arizonia', cursive;
    font-size: 28px;
    color: #6e6e6e;
    letter-spacing: 0.5px;
  }
  .qoute {
    cursor: pointer;
  }
</style>

