<template>
  <div class="col-2 col-md-3 col-lg-2 text-center">
    <div class="card my-card text-secondary p-2">
      <img class="card-img-top" src="../assets/img/logo-small.svg" alt="Card image cap">
      <div class="card-body">
        <h5 class="card-title text-white text-uppercase">Card title</h5>
        <p class="card-text mb-0">Some text.</p>
        <p class="card-text">Some text.</p>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'RecordCard',
}
</script>

<style scoped lang="scss">
@import'../assets/styles/style.scss';
.my-card{
  background-color: #354351;
}
</style>
