<template>
  <div class="hello">
    <div class="card" style="width:20rem;margin:20px 0 24px 0">
      <img class="card-img-top" :src="card.img" alt="image" style="width:100%">
      <div class="card-body">
        <h4 class="card-title">{{card.name}}</h4>
        <p class="card-text">{{card.msg}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    card: Object
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
