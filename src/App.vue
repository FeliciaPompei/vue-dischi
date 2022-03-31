<template>
  <div id="app">
    <Header @selectGenre="seletedGenre"/>
    <RecordList :genreSearch="genreSearch" />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import RecordList from './components/RecordList.vue';

export default {
  name: 'App',
  components: {
    Header,
    RecordList
  },
  data : function() {
    return{
      genreSearch : '',
    }
  },
  methods :  {
    seletedGenre(inputValue){
      console.warn(inputValue);
      this.genreSearch = inputValue;
    }
  },
}
</script>

<style lang="scss">
@import'./assets/styles/style.scss';
body{
  overflow:hidden;
}
</style>
