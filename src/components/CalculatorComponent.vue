<script setup>
import { ref } from 'vue'
const value1 = ref(0)
const formatTooltip = (val) => {
  return val / 100
}
const radio1 = ref('New York')
</script>
<template>
  <div class="main-container">
    <div class="flex-str">
      <div class="slider-block">
        <span class="demonstration">Default value</span>
        <el-slider v-model="value1" />
      </div>
      <div>
        <el-radio-group v-model="radio1" size="large">
          <el-radio-button label="1" />
          <el-radio-button label="2"/>
          <el-radio-button label="3" />
          <el-radio-button label="4+" />
        </el-radio-group>
      </div>
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
}

/* ::v-deep(.el-carousel__item) {
  border-radius: 40px;
 } */

.slider-block {
  display: flex;
  align-items: center;
}
.slider-block .el-slider {
  margin-top: 0;
  margin-left: 12px;
}
.slider-block .demonstration {
  font-size: 14px;
  color: var(--el-text-color-secondary);
  line-height: 44px;
  flex: 1;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  margin-bottom: 0;
}
.slider-block .demonstration + .el-slider {
  flex: 0 0 70%;
}

::v-deep(.el-radio-button) .el-radio-button__inner {
  border-radius: 100%;
  width: 55px;
  height: 55px;
  line-height: 27px;
}
</style>
