<template>
  <main>
    <div id="record-wrapper" class="container w-75 p-4 pb-5">
      <div class="row">
        <div class="col-12 d-flex flex-wrap justify-content-center">
          <RecordCard v-for="(element, index) in searchGenra" :key="index" :record="element"/>
        </div>
      </div>
    </div>
  </main>
</template>

<script>

import RecordCard from './RecordCard.vue'
import axios from 'axios';
export default {
  name: 'RecordList',
  props:['genreSearch'],
  components:{
    RecordCard,
  },
  created: function(){
    setTimeout(this.getRecordList, 3000);
  },
  data: function(){
    return{
      recordList : null,
      filteredGenreList : null,
    }
  },
  methods: {
    getRecordList(){
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((result) => {
        this.recordList = result.data.response;
        this.filteredGenreList = [...this.recordList];
        console.log(this.filteredGenreList)
      })
      .catch((error) => {
        console.error(error);
      })
    }
  },
  computed : {
    searchGenra(){
      if(this.genreSearch == ''){
        return this.filteredGenreList;
      }else{
        return this.filteredGenreList.filter((element) => element.genre.toLowerCase().includes(this.genreSearch.toLowerCase()));
      }
    }
  }
}
</script>

<style scoped lang="scss">
@import'../assets/styles/style.scss';
main {
  background-color: $mainBgColor;
  height: 100vh;
}
</style>
