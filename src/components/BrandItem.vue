<template>
  <div class="item">
    <label>
      <input class="input" type="checkbox">
      <span class="name">
        Бренд
      </span>
      <span class="count">(xxx)</span>
    </label>
  </div>
</template>

<script>

</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.item {
  padding: 5px 0;
}

.name {
  font-family: Open Sans, serif;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 16px;
  color: #000000;
  opacity: 0.7;
}

.input {
  border: 1px solid #E5E5E5;
  border-radius: 3px;
  width: 15px;
  height: 15px;
}

.count {
  font-family: Open Sans, serif;
  font-size: 14px;
  line-height: 16px;
  color: #C4C4C4;
}
</style>
