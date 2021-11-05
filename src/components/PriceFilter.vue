<template>
  <div class="wrap">
    <div class="title">Цена, валюта</div>
    <div class="inputs">
      <div>
        <span>от</span>
        <input class="input" v-model.number="minPrice"/>
      </div>
      <div>
        <span>до</span>
        <input class="input" v-model.number="maxPrice" />
        <span>р</span>
      </div>
    </div>
    <div class="slider">
      <input type="range" min="1000" max="100000" step="1000" v-model.number="minPrice" @change="minMax">
      <input type="range" min="1000" max="100000" step="1000" v-model.number="maxPrice" @change="minMax">
    </div>
  </div>
</template>

<script>

export default {
  methods: {
    minMax() {
      if(this.minPrice > this.maxPrice) {
        let tmp = this.minPrice;
        this.minPrice = this.maxPrice;
        this.maxPrice = tmp;
      }
    }
  },
  data() {
    return {
      minPrice: 1000,
      maxPrice: 100000,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.wrap {
  margin-top: 46px;
  display: flex;
  flex-direction: column;
}

.inputs {
  display: flex;
  flex-wrap: wrap;
}

.inputs span {
  font-family: Arial,serif;
  font-size: 12px;
  line-height: 14px;
  color: #000000;
  opacity: 0.5;
}
.input {
  padding: 12px 13px;
  margin: 10px 5px;
  width: 110px;
  height: 40px;
  border: 1px solid #DEDEDE;
  border-radius: 3px;
  font-family: Arial,serif;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 16px;
  color: #000000;
}
.title {
  margin-bottom: 16px;
}
.slider {
  width: 100%;
  margin: 19px auto;
  text-align: center;
  position: relative;
}
.slider input {
  width: 100%;
  position: absolute;
  left: 0;
  bottom: 0;
}
.slider input::-webkit-slider-thumb {
  z-index: 2;
  position: relative;
}

input[type=range]  {
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
}
input[type=range]::-webkit-slider-runnable-track {
  border-radius: 2px;
  height: 4px;
  background-color: #000000;
}
input[type=range]::-webkit-slider-thumb {
  background: #ffffff;
  border: 2px solid #000000;
  border-radius: 50%;
  cursor: pointer;
  width:14px;
  height: 14px;
  -webkit-appearance: none;
  margin-top: -5px;
}



</style>
