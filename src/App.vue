<template>
  <div id="app">
    <Header/>
    <Main/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';
import axios from 'axios';

export default {
  name: 'App',
  components: {
    Header,
    Main
  },
  created: function(){
    this.getRecordList()
  },
  methods: {
    getRecordList(){
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((result) => {
        console.table(result.data.response)
      })
      .catch((error) => {
        console.error(error);
      })
    }
  }
}
</script>

<style lang="scss">
@import'./assets/styles/style.scss';
body{
  overflow:hidden;
}
</style>
