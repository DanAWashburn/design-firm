<template>
<section class="container">
  <div class="flex-item">
    <img src="../static/house-one.png" class="sample">
    <img src="../static/house-two.png" class="sample">
    <img src="../static/house-three.png" class="sample">
  </div>
</section>
</template>

<script>
export default {
  head() {
    return {
      title: this.title,
      meta: [{
        hid: 'design firm architects',
        name: 'home of design firm architects',
        content: 'Example projects of modern architecture'
      }]
    }
  }
}
</script>

<style lang="scss">
.sample {
    padding: 0;
    border: 2px solid black;
    margin: 15px;
}
</style>
