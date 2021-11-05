<template>
  <div class="wrap">
    <div class="tab">Сортировать по:</div>
    <div v-for="item in items" class="tab">
      <span v-if="item.active" class="text active">
        {{ item.title }}
      </span>
      <span v-else class="text">
         {{ item.title }}
      </span>
    </div>
    <div class="show">
      <span>показывать по </span>
      <select>
        <option>1</option>
        <option>2</option>
      </select>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {active: true, title: 'популярности'},
        {active: false, title: 'сначала дешевые'},
        {active: false, title: 'сначала дорогие'}
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.wrap {
  margin-bottom: 10px;
  padding-left: 20px;
  display: flex;
  align-items: center;
}

.tab {
  margin-right: 10px;
  font-family: Open Sans, serif;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 19px;
  color: #000000;
}

.text:not(.active):hover {
  cursor: pointer;
}

.text {
  font-family: Open Sans, serif;
  color: #5375B7;
}

.text.active {
  color: #333333;
  border-bottom: 1px solid #F1BD45;
}

.show {
  margin-left: auto;
  margin-right: 20px;
}

.show span {
  font-family: Open Sans, serif;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 19px;
  color: #000000;
}

select {
  padding: 6px 10px;
  border: 1px solid #DEDEDE;
  border-radius: 3px;
  font-family: Open Sans, serif;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 19px;
  color: #000000;
}
</style>
