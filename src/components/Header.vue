<template>
  <header class="container-fluid">
    <div class="row align-items-center justify-content-between p-2">
      <div class="col-2">
        <img class="img-fluid w-25 p-2" src="../assets/img/logo-small.svg" alt="Spotify Logo">
      </div>
      <div class="col-2 p-0 d-flex">
        <select class="form-select p-0 text-center w-75 me-2" v-model="selected">
          <option value="" selected>Show all</option>
          <option value="rock">Rock</option>
          <option value="pop">Pop</option>
          <option value="jazz">Jazz</option>
          <option value="metal">Metal</option>
        </select>
        <!-- quando clicco su il bottone mi si cerca il value  -->
        <button class="btn btn-info" 
        @click="$emit('selectGenre', selected)">
          Search
        </button>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderIndex',
  data : function(){
    return{
      selected : '',
    }
  }
}
</script>

<style scoped lang="scss">
@import'../assets/styles/style.scss';

header {
  background-color: $headerBgColor;
}
</style>
