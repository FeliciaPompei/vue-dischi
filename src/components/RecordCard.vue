<template>
  <div class="col-2 col-md-3 col-lg-2 text-center">
    <div class="card my-card text-secondary p-2">
      <img class="card-img-top" :src="element.poster" :alt="element.title">
      <div class="card-body">
        <h5 class="card-title text-white text-uppercase"> {{element.title}} </h5>
        <p class="card-text mb-0"> {{element.author}} </p>
        <p class="card-text"> {{element.year}} </p>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'RecordCard',
  props : {'element': Object }
}
</script>

<style scoped lang="scss">
@import'../assets/styles/style.scss';
.my-card{
  background-color: #354351;
}
</style>
