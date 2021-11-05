<template>
  <div class="wrapper">
    <form class="wrap">
      <label class="search">
        <input class="input" placeholder="Введите запрос"/>
        <span class="placeholder"></span>
      </label>
      <button class="btn">Найти</button>
      <button class="close">Закрыть</button>
    </form>
  </div>
</template>

<script>

</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.wrap {
  display: flex;
}

.input {
  width: 100%;

  padding: 13px 13px 13px 56px;
  border-top: 1px solid #C7C7C7;
  border-bottom: 1px solid #C7C7C7;
  border-left: 1px solid #C7C7C7;
  border-right: none;
  border-radius: 5px 0 0 5px;
  height: 40px;
  font-family: Arial, serif;
  font-size: 14px;
  line-height: 16px;
  color: #000000;
  /*position: relative;*/
}

.search {
  flex: 0 1 78%;
  position: relative;
}

.placeholder {
  position: absolute;
  height: 17px;
  width: 29px;
  top: 11px;
  left: 15px;
  bottom: 11px;

  padding-right: 12px;
  border-right: 1px solid rgba(0, 0, 0, 0.5);
  background-image: url("../assets/search.png");
  background-repeat: no-repeat;
}

.btn {
  flex: 0 1 12%;
  height: 40px;
  background: #F1BD45;
  border-radius: 0 3px 3px 0;
  border: none;
  font-family: Arial, serif;
  font-size: 14px;
  line-height: 16px;
  text-align: center;
  color: #000000;
}

.btn:hover {
  cursor: pointer;
}

.close:hover {
  cursor: pointer;
}

.close {
  flex: 0 1 9%;
  /*margin-left: 10px;*/
  margin-left: auto;
  height: 40px;
  border: 1px solid #DEDEDE;
  border-radius: 3px;
  background: #ffffff;
  /*width: 9%;*/
  font-family: Arial, serif;
  font-size: 14px;
  line-height: 16px;
  text-align: center;
  color: #000000;
}


@media screen and (max-width: 767px) {
  /* стили для средних планшетов - начало */
  .search {
    flex: 0 1 50%;
  }

  .btn {
    flex: 0 1 23%;
  }

  .close {
    flex: 0 1 23%;
  }
}
</style>