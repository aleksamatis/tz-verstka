<template>
  <div class="main-container">
    <img class="main-container-down" src="@/assets/images/detail.svg" />
    <img class="main-container-upper" src="@/assets/images/detailarrow.svg" />
  </div>
  <div class="main-container-small">
    <img class="main-container-down" src="@/assets/images/detail2.svg" />
    <img class="main-container-upper" src="@/assets/images/detailarrow2.svg" />
  </div>
</template>

<style scoped>
.main-container {
  display: flex;
  justify-content: center;
}
.main-container-down {
  position: relative;
  z-index: 0;
}
.main-container-upper {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
.main-container-small {
  display: none;
}

@media (max-width: 1085px) {
  .main-container {
    display: none;
  }
  .main-container-small {
    display: block;
    display: flex;
    justify-content: center;
    z-index: -10;
  }
}
</style>
