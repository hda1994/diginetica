<template>
  <div class="wrapper">
    <CategoryItem v-for="item in items"/>
  </div>
</template>

<script>
import CategoryItem from './CategoryItem';

export default {
  components: {
    CategoryItem
  },
  data() {
    return {
      items: [1, 2, 3, 4, 5, 6, 7, 8]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.wrapper {
  display: flex;
  margin: 0 -10px;
  flex-wrap: wrap;
}
</style>
