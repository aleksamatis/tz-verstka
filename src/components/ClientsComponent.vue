<template>
  <div class="main-container">
    <div>
      <img src="@/assets/images/clients.svg" alt="" />
    </div>
    <div class="team-members-item">
      <div><img src="@/assets/images/client1.jpg" alt="" /></div>
      <div>Белякинов</div>
      <div>Ярослав</div>
      <div class="item-description">Евроремонт</div>
    </div>
    <div class="team-members-item">
      <div><img src="@/assets/images/client2.jpg" alt="" /></div>
      <div>Сорокина</div>
      <div>Ольга</div>
      <div class="item-description">Евроремонт</div>
    </div>
    <div class="team-members-item">
      <div><img src="@/assets/images/client3.jpg" alt="" /></div>
      <div>Самсонов</div>
      <div>Кирилл</div>
      <div class="item-description">Евроремонт</div>
    </div>
  </div>
</template>

<style scoped>
.main-container {
  display: flex;
  justify-content: space-between;
}
.team-members-item {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(7.5px);
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  color: #fff;
  padding: 20px;
  text-align: center;
  font-size: 10px;
  width: 130px;
  height: 150px;
}

.team-members-item .item-description {
  color: rgba(255, 255, 255, 0.7);
}

.team-members-item img {
  border-radius: 100%;
}
</style>
