<script setup>
import BaseIcon from './BaseIcon.vue'
import { reactive } from 'vue'
const objects = reactive([
  {
    icon: 'day',
    title: 'Adjust Lighting',
    desc: 'When caring for indoor plants, make sure the room temperature is neither too cold nor too hot'
  },
  {
    icon: 'water',
    title: "Don't water too often",
    desc: 'Watering ornamental plants indoors does not have to be done every day.'
  },
  {
    icon: 'pot',
    title: "Don't water too often",
    desc: 'Watering ornamental plants indoors does not have to be done every day.'
  },
  {
    icon: 'temperature',
    title: 'Fertilize regularly',
    desc: 'The nutrients most indoor houseplants need are nitrogen for balance and potassium for stem strength'
  }
])
</script>

<template>
  <section class="care">
    <div class="care__container">
      <div class="care__row">
        <div class="care__content">
          <div class="care__content-top">
            <div class="care__content-title">
              How to care <br />
              for plants
            </div>
            <div class="care__content-desc">Take care of plants with all your heart</div>
          </div>
          <div class="care__body body">
            <div v-for="item in objects" :key="item.icon" class="body__row">
              <div class="body__icon">
                <BaseIcon :name="item.icon" />
              </div>
              <div class="body__content">
                <div class="body__title">{{ item.title }}</div>
                <div class="body__desc">{{ item.desc }}</div>
              </div>
            </div>
          </div>
        </div>
        <div class="care__image">
          <img src="../assets/img/care.png" alt="" />
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.care {
  padding-bottom: 100px;
  &__container {
    max-width: 1400px;
    margin: 0 auto;
    overflow: hidden;
    padding: 0 10px;
  }
  &__row {
    display: flex;
    justify-content: space-between;
    @media (max-width: 768px) {
      flex-direction: column-reverse;
      flex-wrap: wrap;
    }
  }
  &__content {
    display: flex;
    flex-direction: column;
    gap: 50px;
    flex: 0 0 50%;
    @media (max-width: 768px) {
      gap: 15px;
      justify-content: center;
      width: 100%;
    }
  }
  &__content-top {
    text-align: center;
  }
  &__content-title {
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 500;
    font-size: 54px;
    line-height: 75px;
    color: #081323;
    padding-bottom: 10px;
    @media (max-width: 1024px) {
      br {
        display: none;
      }
      font-size: 45px;
      line-height: 60px;
    }
    @media (max-width: 850px) {
      font-size: 36px;
      padding-bottom: 2px;
    }
    @media (max-width: 768px) {
      font-size: 27px;
    }
  }
  &__content-desc {
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 400;
    font-size: 24px;
    line-height: 28px;
    color: #4f4f4f;
    @media (max-width: 1024px) {
      font-size: 20px;
    }
  }
  &__body {
  }
  &__image {
    padding-top: 80px;
    width: 100%;
    height: 100%;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center;
    }
  }
}
.body {
  width: 100%;
  &__row {
    display: flex;
    align-items: center;
    gap: 20px;
    padding: 10px 0;
    @media (max-width: 768px) {
      padding: 10px;
      justify-content: center;
    }
    @media (max-width: 320px) {
      flex-direction: column;
      justify-content: center;
      padding: 10px;
    }
  }
  &__icon {
    @media (max-width: 1024px) {
      width: 50px;
      height: 50px;
    }
    @media (max-width: 768px) {
      width: 45px;
      height: 45px;
    }
  }
  &__content {
    flex: 0 0 70%;
    justify-content: center;
    // @media (max-width: 768px) {
    //   flex: 0 0 90%;
    // }
    @media (max-width: 320px) {
      flex: 0 0 80%;
      text-align: center;
    }
  }
  &__title {
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 500;
    font-size: 32px;
    line-height: 38px;
    color: #000000;
    padding-bottom: 8px;
    @media (max-width: 1024px) {
      font-size: 30px;
      padding-bottom: 5px;
    }
    @media (max-width: 850px) {
      font-size: 27px;
    }
    @media (max-width: 768px) {
      font-size: 24px;
    }
  }
  &__desc {
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 400;
    font-size: 20px;
    line-height: 33px;
    color: #4f4f4f;
    @media (max-width: 1024px) {
      font-size: 14px;
      line-height: 30px;
    }
  }
}
</style>
