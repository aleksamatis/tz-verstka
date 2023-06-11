<script setup>
import FormSubmissionComponent from '@/components/FormSubmissionComponent.vue'
import HeaderNavComponent from '@/components/HeaderNavComponent.vue'
import CardsContentComponent from '@/components/CardsContentComponent.vue'
import ClientsComponent from '@/components/ClientsComponent.vue'
import CalculatorComponent from '@/components/CalculatorComponent.vue'
</script>

<template>
  <header>
    <HeaderNavComponent />
    <div class="header-content">
      <div class="header-left-wrap">
        <div class="header-left">
          <FormSubmissionComponent />
          <ClientsComponent />
        </div>
        <CalculatorComponent />
      </div>
    </div>
  </header>
  <DetailDesignComponent />
  <CardsContentComponent />
</template>

<style scoped>
header {
  background: linear-gradient(
    293.29deg,
    #0a2756 1.86%,
    #1f1f1f 31.03%,
    #1f1f1f 53.19%,
    #1f1f1f 77.76%,
    #0a2756 107.16%
  );
}

@media (max-width: 1770px){
    header {
        padding-left: 60px;
        padding-right: 60px;
    }
  }

@media (max-width: 1085px){
  header {
      padding-left: 83px;
      padding-right: 83px;
  }
}

.header-content > div {
  display: flex;
  max-width: 1170px;
  margin: 0 auto;
}

.header-left {
  padding-right: 49px;
}

@media (max-width: 1085px){
    .header-left-wrap {
        flex-wrap: wrap;
    }
}
</style>
