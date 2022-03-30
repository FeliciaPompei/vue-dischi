<template>
  <div id="record-wrapper" class="container w-75 p-5">
    <div class="row">
          <RecordCard />
    </div>
  </div>
</template>

<script>

import RecordCard from './RecordCard.vue'
export default {
  name: 'RecordList',
  components:{
    RecordCard,
  }
}
</script>

<style scoped lang="scss">
@import'../assets/styles/style.scss';
</style>
