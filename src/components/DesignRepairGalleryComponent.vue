<script setup>
import {ref} from 'vue';

const itemIndex = ref(0)
</script>
<template>
  <div>
    <div class="main-container">
      <div class="main-container-transformed-2"></div>
      <div class="main-container-transformed"></div>
      <div class="main-gallery">
        <el-carousel indicator-position="outside" initial-index="itemIndex" @change="itemIndex = $event + 1" autoplay="false" height="369px">
          <el-carousel-item v-for="item in 4" :key="item">
            <img src="@/assets/images/image1.jpg" alt=""/>
          </el-carousel-item>
        </el-carousel>
        
        <div class="title">Дизайнерский ремонт</div>
        <div class="description-gallery-counter">
        <div class="description">ЖК «Пироговская Ривьера», 104 м²</div>
        <div class="gallery-counter"><span class="gallery-counter-changed">{{ itemIndex }}</span><span class="gallery-counter-number">/6</span></div>
        </div>
      </div>
     
    </div>
  </div>
</template>

<style scoped>
.main-gallery {
  width: 480px;
  aspect-ratio: 0.8;
  height: 516px;
  padding: 25px;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(5px);
  border-radius: 40px;
}
.main-container {
  position: relative;
}

.main-gallery div.title {
  color: #fff;
  font-family: 'Prosto One';
  font-style: normal;
  font-weight: 400;
  font-size: 25px;
  line-height: 31px;
  text-transform: capitalize;
  text-align: left;
}
.main-gallery div.description {
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 19px;
  color: rgba(255, 255, 255, 0.7);
  display: flex;
}
.main-gallery div.gallery-counter {
  font-family:'Prosto One';
  color: #fff;
}
.description-gallery-counter{
  display: flex;
  justify-content: center;
  text-align: center;
  justify-content: space-between;
}
.gallery-counter-changed {
  font-size: 35px;
}

.gallery-counter-number {
  color:#C3C3C3;
}
.el-carousel__item h3 {
    color: #475669;
    font-size: 66px;
    opacity: 0.75;
    line-height: 300px;
    margin: 0;
  }

::v-deep(.el-carousel__item) {
  border-radius: 40px;
 }

 .main-container-transformed {
    width: 480px;
    height: 516px;
    background: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(5px);
    border-radius: 40px;
    transform: rotate(10.46deg);
    position: absolute;
    top: 30px;
    left: 60px;
 }

 .main-container-transformed-2 {
    width: 480px;
    height: 516px;
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(5px);
    border-radius: 40px;
    transform: rotate(19.61deg);
    position: absolute;
    top: 60px;
    left: 90px;
 }

.el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
  }

  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
  }
</style>
