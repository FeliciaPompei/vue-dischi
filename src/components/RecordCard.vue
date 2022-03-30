<template>
  <div class="my-card text-secondary p-2 m-2 text-center">
    <img class="card-img-top p-2" :src="element.poster" :alt="element.title">
    <div class="card-body p-2">
      <h6 class="card-title text-white text-uppercase"> {{element.title}} </h6>
      <p class="card-text mb-0"> {{element.author}} </p>
      <p class="card-text"> {{element.year}} </p>
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
  font-size: 0.7rem;
  width:calc(80% / 5);
}
</style>
