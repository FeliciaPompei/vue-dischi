<template>
  <main>
    <RecordList/>
  </main>
</template>

<script>
import RecordList from './RecordList.vue'
export default {
  name: 'MainIndex',
  components : {
    RecordList,
  }
}
</script>

<style scoped lang="scss">
@import'../assets/styles/style.scss';
main {
  background-color: $mainBgColor;
  height: calc(100vh - 50px);
}
</style>
