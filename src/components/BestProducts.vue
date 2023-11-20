<script setup>
import BaseIcon from './BaseIcon.vue'
import { reactive } from 'vue'
const products = reactive([
  {
    image: 'plant_1.png',
    count: '$65.00'
  },
  {
    image: 'plant_2.png',
    count: '$65.100'
  },
  {
    image: 'plant_3.png',
    count: '$650.00'
  }
])
</script>

<template>
  <main class="best-product">
    <div class="best-product__container">
      <div class="best-product__row">
        <div class="best-product__content">
          <div class="best-product__title">Best Seller Product</div>
          <button class="best-product__sub-title">
            <p>See all colection</p>
            <BaseIcon name="arrowRight" />
          </button>
        </div>
        <div class="best-product__columns">
          <div v-for="item in products" :key="item.title" class="best-product__body">
            <div class="best-product__image">
              <img :src="require(`../assets/img/${item.image}`)" alt="" />
            </div>
            <div class="best-product__sub-body sub-body">
              <div class="sub-body__title">
                Cammile
                <div class="sub-body__stars">
                  <BaseIcon name="star" />
                  <BaseIcon name="star" />
                  <BaseIcon name="star" />
                  <BaseIcon name="star" />
                  <BaseIcon name="star" />
                </div>
              </div>
              <div class="sub-body__count-plus">
                <p>{{ item.count }}</p>
                <BaseIcon name="plus" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
.best-product {
  padding-bottom: 50px;
  &__container {
    max-width: 1400px;
    margin: 0 auto;
    padding: 0 10px;
  }
  &__row {
    display: flex;
    align-items: center;
    justify-content: space-around;
    @media (max-width: 1150px) {
      flex-wrap: wrap;
      flex-direction: column-reverse;
    }
  }
  &__content {
    display: flex;
    flex-direction: column;
    padding: 10px;
    @media (max-width: 1150px) {
      text-align: center;
      flex: 0 0 100%;
    }
  }
  &__title {
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 500;
    font-size: 64px;
    line-height: 75px;
    color: #081323;
    @media (max-width: 375px) {
      br {
        display: none;
      }
      font-size: 29px;
    }
  }
  &__sub-title {
    background-color: transparent;
    display: flex;
    align-items: center;
    padding-left: 5px;
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 500;
    font-size: 24px;
    line-height: 28px;
    color: #4f4f4f;
    @media (max-width: 1150px) {
      justify-content: center;
      font-size: 20px;
    }
    p {
      margin: 0;
    }
  }
  &__columns {
    display: flex;
    gap: 32px;
    padding: 10px;
    @media (max-width: 815px) {
      flex-wrap: wrap;
      justify-content: center;
      flex: 0 0 100%;
    }
  }
  &__body {
    position: relative;
    display: flex;
    flex-direction: column;
    gap: 10px;
    @media (max-width: 815px) {
      padding-bottom: 75px;
    }
  }
  &__image {
    padding-bottom: 55px;
    margin-top: -116px;
    img {
      width: 100%;
      height: 100%;
      object-position: center;
      object-fit: cover;
    }
    &::after {
      content: '';
      position: absolute;
      z-index: -1;
      top: 0;
      left: 0;
      width: 100%;
      height: 300px;
      background: #c1d0e4;
      border-radius: 50px;
    }
  }
  &__sub-body {
  }
}
.sub-body {
  background: #ffffff;
  border-radius: 50px;
  padding: 25px;
  margin-top: -60px;
  &__title {
    display: flex;
    flex-direction: column;
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 500;
    font-size: 32px;
    line-height: 38px;
    color: #081323;
  }
  &__stars {
    display: flex;
    align-items: center;
    flex: 1 1 auto;
    padding-bottom: 20px;
  }
  &__count-plus {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 30px;
    p {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 500;
      font-size: 32px;
      line-height: 38px;
      color: #081323;
    }
    span {
      cursor: pointer;
    }
  }
}
</style>
