<script setup>
import BaseIcon from './BaseIcon.vue'
import { ref } from 'vue'
const products = ref([
  {
    icon: 'box',
    title: 'Free Shapping',
    subTitle: ''
  },
  {
    icon: 'payment',
    title: 'Quick Payment',
    subTitle: '100% secure payment'
  },
  {
    icon: 'support',
    title: '24/7 Support',
    subTitle: 'Quick support'
  }
])
</script>

<template>
  <section class="free">
    <div class="free__container">
      <div class="free__row">
        <div v-for="item in products" :key="item.title" class="free__body">
          <div class="free__icon">
            <BaseIcon :name="item.icon" />
          </div>
          <div class="free__title_box">
            <div class="free__title">{{ item.title }}</div>
            <div class="free__sub_title">{{ item.subTitle }}</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.free {
  padding-bottom: 250px;
  &__container {
    max-width: 1400px;
    margin: 0 auto;
    overflow: hidden;
    padding: 0 10px;
  }
  &__row {
    display: flex;
    align-items: center;
    justify-content: space-around;
    @media (max-width: 880px) {
      padding: 10px;
      flex-wrap: wrap;
      gap: 20px;
    }
    @media (max-width: 690px) {
      flex-direction: column;
      justify-content: center;
    }
  }
  &__body {
    display: flex;
    align-items: center;
    gap: 20px;
    @media (max-width: 320px) {
      width: 100%;
      justify-content: space-between;
    }
  }
  &__icon {
    @media (max-width: 500px) {
      width: 70px;
      height: 70px;
    }
  }
  &__title_box {
  }
  &__title {
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 500;
    font-size: 32px;
    line-height: 38px;
    color: #081323;
    padding-bottom: 10px;
    @media (max-width: 500px) {
      font-size: 25px;
    }
  }
  &__sub_title {
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 500;
    font-size: 20px;
    line-height: 23px;
    color: #828282;
    @media (max-width: 500px) {
      font-size: 15px;
    }
  }
}
</style>
