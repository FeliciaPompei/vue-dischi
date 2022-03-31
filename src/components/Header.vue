<template>
  <header class="container-fluid">
    <div class="row align-items-center">
      <div class="col-2">
        <img class="img-fluid w-25 p-2" src="../assets/img/logo-small.svg" alt="Spotify Logo">
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
  background-color: $headerBgColor;
  height: 50px;
}
</style>
