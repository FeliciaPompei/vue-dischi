<template>
  <div id="record-wrapper" class="container w-75 p-5">
    <div class="row">
      <div class="col-12 d-flex flex-wrap justify-content-center">
        <RecordCard v-for="(element, index) in recordList" :key="index" :element="element"></RecordCard>
      </div>
    </div>
  </div>
</template>

<script>

import RecordCard from './RecordCard.vue'
import axios from 'axios';
export default {
  name: 'RecordList',
  components:{
    RecordCard,
  },
  created: function(){
    this.getRecordList()
  },
  data: function(){
    return{
      recordList : null,
    }
  },
  methods: {
    getRecordList(){
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((result) => {
        console.log(result.data.response)
        this.recordList = result.data.response;
        console.log(this.recordList)
      })
      .catch((error) => {
        console.error(error);
      })
    }
  }
}
</script>

<style scoped lang="scss">
@import'../assets/styles/style.scss';
</style>
