<script setup>
import { ref } from 'vue'
const value = ref(true)
const value5 = ref('')
const value1 = ref(0)
const value2 = ref(true)
const value3 = ref(true)
const formatTooltip = (val) => {
  return val / 100
}
const radio1 = ref('New York')
const radio2 = ref('New York')

const options = [
  {
    value: 'Option1',
    label: 'Option1',
  },
  {
    value: 'Option2',
    label: 'Option2',
  },
  {
    value: 'Option3',
    label: 'Option3',
  },
  {
    value: 'Option4',
    label: 'Option4',
  },
]
</script>
<template>
  <div class="main-container">
    <div class="flex-str">
      <div>
        <div class="calculator-title">Площадь квартиры:</div>
        <div class="vol-slider"></div>
        <div class="slider-block">
          <el-slider v-model="value1" />
        </div>
      </div>
      <div class="calculator-radio">
        <div class="calculator-title">Количество комнат:</div>
        <el-radio-group v-model="radio1" size="large">
          <el-radio-button label="1" />
          <el-radio-button label="2"/>
          <el-radio-button label="3" />
          <el-radio-button label="4+" />
        </el-radio-group>
      </div>
    </div>
    <div class="flex-str">
    <div class="flex-str-special">
      <div class="calculator-radio-what-flat">
        <div class="calculator-title">Какая квартира?:</div>
        <el-radio-group v-model="radio2" size="large">
          <el-radio-button label="1" />
          <el-radio-button label="2"/>
        </el-radio-group>
      </div>
      <div>
        <div>
        <el-switch
          v-model="value"
          size="large"
        /><span class="switch-text">Черновые материалы</span>
        </div>
        <div>
        <el-switch
          v-model="value2"
          size="large"
        /><span class="switch-text">Чистовые материалы</span>
        </div>
        <div>
        <el-switch
          v-model="value3"
          size="large"
        /><span class="switch-text">Дизайн-проект</span>
        </div>
      </div>
    </div>
    <el-select v-model="value5" class="m-2" placeholder="Select" size="large">
    <el-option
      v-for="item in options"
      :key="item.value"
      :label="item.label"
      :value="item.value"
    />
    </el-select>
  </div>
  </div>
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

.flex-str div {
  flex: 1;
}

.vol-slider {
  height: 55px;
  background: #3A3A3A;
  border: 1px solid #818181;
  box-shadow: inset 0px 0px 15px 11px rgba(0, 0, 0, 0.17);
  border-radius: 60px;
  position: relative;
}
.slider-block {
  position: absolute;
  align-items: center;
  width: 100%;
  bottom: 0;
}
.slider-block .el-slider {
  margin-top: 0;
  margin-left: 12px;
  height: 0;
}
::v-deep(.el-radio-button) .el-radio-button__inner {
  border-radius: 100%;
  width: 55px;
  height: 55px;
  line-height: 27px;
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
</style>
