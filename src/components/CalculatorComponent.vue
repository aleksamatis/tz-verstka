<script setup>
import { ref } from 'vue'
import InputWithSlider from './InputWithSlider.vue'
import CalculatorRooms from './CalculatorRooms.vue'

const squareValue = ref(0)

const value = ref(true)
const value2 = ref(true)
const value3 = ref(true)
const flatType = ref('1')
</script>
<template>
  <form class="main-container">
    <div class="flex-str">
      <div>
        <div class="calculator-title">Площадь квартиры:</div>
        <InputWithSlider v-model="squareValue" />
      </div>
      <CalculatorRooms />
    </div>
    <div class="flex-str">
      <div class="flex-str-special">
        <div class="calculator-radio-what-flat">
          <div class="calculator-title">Какая квартира?:</div>
          <el-radio-group v-model="flatType">
            <el-radio-button label="1">Вторичка</el-radio-button>
            <el-radio-button label="2">Новостройка</el-radio-button>
          </el-radio-group>
        </div>
        <div>
          <div>
            <el-switch v-model="value" size="large" /><span class="switch-text"
              >Черновые материалы</span
            >
          </div>
          <div>
            <el-switch v-model="value2" size="large" /><span class="switch-text"
              >Чистовые материалы</span
            >
          </div>
          <div>
            <el-switch v-model="value3" size="large" /><span class="switch-text"
              >Дизайн-проект</span
            >
          </div>
        </div>
      </div>
      <RenovationType />
    </div>
  </form>
</template>

<style scoped>
.main-container {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(5px);
  border-radius: 40px;
  padding: 30px;
}

.flex-str {
  display: flex;
  width: 100%;
  justify-content: space-between;
  padding-bottom: 27px;
  gap: 30px;
}

.flex-str-special {
  display: flex;
  width: 100%;
  align-items: start;
  flex-direction: column;
}

.switch-text {
  font-size: 14px;
  line-height: 16px;
  color: rgba(255, 255, 255, 0.7);
}

.flex-str > div {
  flex: 1;
}

.calculator-radio-what-flat ::v-deep(.el-radio-button) .el-radio-button__inner {
  width: 115px;
  height: 55px;
  border-radius: 60px;
}
.calculator-title {
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 19px;
  color: #fff;
  padding-bottom: 10px;
}

@media (max-width: 1085px) {
  .main-container {
    padding: 20px;
  }

  .flex-str {
    display: block;
  }
}
</style>
