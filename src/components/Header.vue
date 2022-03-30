<template>
  <header class="container-fluid">
    <div class="row align-items-center">
      <div class="col-2">
        <img class="img-fluid" src="../assets/img/logo-small.svg" alt="Spotify Logo">
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderIndex',
}
</script>

<style scoped lang="scss">
@import'../assets/styles/style.scss';

header {
  background-color: $headerColor;
  img{
    width:25%;
    padding: 0.5rem;
  }
}
</style>
