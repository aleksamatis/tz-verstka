<template>
  <div class="main-container">
    <div class="cards-content">
      <div class="cards-content-item">
        <div>
          <div class="cards-content-item-complectator">
            Комплектатор
            <div class="cards-content-item-design"></div>
          </div>
          <span>бесплатно</span> подберет чистовой материал <span>за 1 час</span> в шоуруме
        </div>
        <button class="btn">Узнать подробнее</button>
      </div>
      <div class="cards-content-item-3">
        <h2>Подберем, доставим</h2>
        <span>черновой материал со склада,<br />отчитаемся и выкупим остатки</span>
      </div>
      <div class="cards-content-item-2">
        <h2>Поможем</h2>
        <span>с дизайном и планировкой.<br />Проследим за реализацией<br />во время ремонта</span>
      </div>
      <div class="cards-content-item-1">
        <h2>Сделаем мебель</h2>
        <span
          >и кухонный гарнитур по ценам 7-10%<br />ниже рынка. Своё производство, склад<br />и
          шоурум</span
        >
      </div>
    </div>
  </div>
</template>

<style scoped>
.cards-content-item-complectator {
  display: flex;
  align-items: center;
}
.cards-content-item-design {
  background: transparent;
  border: 2px solid #0975a3;
  width: 148.42px;
  height: 27.51px;
  border-radius: 60px;
}
.cards-content {
  display: flex;
  justify-content: space-between;
  max-width: 1170px;
  margin: 0 auto;
  flex-wrap: wrap;
}
.cards-content > div {
  width: 50%;
}
.cards-content-item {
  width: 570px;
}
.cards-content-item-1 {
  width: 570px;
  height: 261px;
  border-radius: 30px;
  padding: 30px;
  background-repeat: no-repeat;
  background-position: right;
  background: url('@/assets/images/backgroundimg1.svg'),
    linear-gradient(282.48deg, rgba(9, 117, 163, 0.89) -2.44%, rgba(101, 165, 255, 0.52) 105.31%);
}

.cards-content-item-2 {
  width: 570px;
  height: 261px;
  border-radius: 30px;
  padding: 30px;
  background: url('@/assets/images/backgroundimg2.svg'),
    linear-gradient(282.45deg, #052e74 -2.73%, #202020 105.3%);
  background-repeat: no-repeat;
  background-position: right;
  background-position-y: bottom;
}

.cards-content-item-3 {
  width: 570px;
  height: 261px;
  border-radius: 30px;
  padding: 30px;
  background: url('@/assets/images/backgroundimg3.svg'),
    linear-gradient(282.48deg, #e7f6ff -2.44%, rgba(243, 243, 243, 0.5) 105.31%);
  background-repeat: no-repeat;
  background-position: right;
}

.cards-content h2 {
  font-family: 'Prosto One';
  font-weight: 400px;
  font-size: 25px;
  line-height: 30.62px;
}

.cards-content span {
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 15px;
}
.cards-content .cards-content-item-2 h2 {
  font-family: 'Prosto One';
  font-weight: 400px;
  font-size: 25px;
  line-height: 30.62px;
  color: #fff;
}

.cards-content .cards-content-item-2 span {
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 15px;
  color: #fff;
}
.btn {
  background: linear-gradient(
    92.78deg,
    rgba(30, 106, 214, 0.88) -0.27%,
    rgba(11, 116, 168, 0.88) 100%
  );
  border-radius: 60px;
  border: 2px solid #2168de;
  color: #fff;
  font-size: 14px;
  border-radius: 60px;
  cursor: pointer;
  width: 280px;
  height: 60px;
}
.cards-content-item div {
  font-family: 'Prosto One';
  font-style: normal;
  font-weight: 400;
  font-size: 38px;
  line-height: 47px;
  text-transform: uppercase;
}

.cards-content-item div span {
  color: #2168de;
  font-family: 'Prosto One';
  font-style: normal;
  font-weight: 400;
  font-size: 38px;
  line-height: 47px;
  text-transform: uppercase;
}

@media (max-width: 1170px) {
  .main-container .cards-content {
    padding-left: 60px;
    padding-right: 60px;
  }
}

@media (max-width: 1085px) {
  .main-container .cards-content {
    flex-wrap: wrap;
    justify-content: center;
    padding-left: 83px;
    padding-right: 83px;
  }

  .cards-content-item div {
    font-size: 18px;
  }

  .cards-content-item div span {
    font-size: 18px;
  }

  .btn {
    width: 100%;
  }
}
</style>
