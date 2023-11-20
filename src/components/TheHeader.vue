<script setup>
import { reactive, ref } from 'vue'
import AgonLogo from '@/components/base/AgonLogo.vue'
import BaseIcon from './BaseIcon.vue'
const menuItems = reactive([
  { id: 0, title: 'Home', activeClass: true },
  { id: 1, title: 'Shop' },
  { id: 2, title: 'About Us' },
  { id: 3, title: 'Contact' }
])

const activeBurger = ref(false)
const scrollTrigger = ref(80)
window.onscroll = function () {
  window.scrollY >= scrollTrigger.value || window.pageYOffset >= scrollTrigger.value
    ? document.querySelector('.header').classList.add('scroll')
    : document.querySelector('.header').classList.remove('scroll')
}
</script>
<template>
  <div :class="['header', { active: activeBurger }]">
    <div class="header__container">
      <div class="header__row">
        <div class="header__logo">
          <AgonLogo />
        </div>
        <div class="header__body">
          <ul class="header__menu">
            <li v-for="item in menuItems" :key="item.title" class="header__item">
              <a href="" :class="['header__link ', { active_link: item.activeClass }]">
                {{ item.title }}
              </a>
            </li>
          </ul>
        </div>
        <div class="header__chart">
          <BaseIcon name="chart" />
        </div>
        <div class="header__burger" @click="activeBurger = !activeBurger">
          <BaseIcon :name="activeBurger ? 'close' : 'burger'" />
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.header {
  position: fixed;
  padding: 10px 5px;
  top: 0;
  left: 0;
  z-index: 10;
  width: 100%;
  transition: 0.3s ease 0s;
  @media (max-width: 450px) {
    padding: 30px 0;
  }
  &.active {
    .header__logo {
      @media (max-width: 850px) {
        display: none;
      }
    }
    .header {
    }

    .header__body {
      @media (max-width: 850px) {
        background-color: #000;
        left: 0;
        transition: left 0.3s;
      }
    }
    .header__menu {
      @media (max-width: 850px) {
        padding-top: 70px;
        display: flex;
        flex-direction: column;
        align-items: center;
        z-index: 3;
        gap: 50px;
      }
    }
    .header__link {
      font-size: 25px;
    }
    .header__btn {
      @media (max-width: 850px) {
        display: none;
      }
    }
  }
  &__container {
    max-width: 1400px;
    margin: 0 auto;
    overflow: hidden;
    padding: 2px 10px;
  }
  &__burger {
    display: none;
    color: #fff;
    @media (max-width: 850px) {
      display: inline;
      position: relative;
      z-index: 10;
    }
  }
  &__logo {
    @media (max-width: 350px) {
      width: 130px;
    }
  }
  &__row {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  &__body {
    @media (max-width: 850px) {
      position: fixed;
      width: 100%;
      left: -100%;
      transition: left 0.3s ease 0s;
      top: 0;
      background-color: #fff;
      height: 100%;
      z-index: 2;
    }
  }

  &__menu {
    display: flex;
    align-items: center;
    gap: 60px;
    list-style: none;
    padding: 0;
    @media (max-width: 850px) {
      display: none;
    }
  }

  &__link {
    &.active_link {
      background: linear-gradient(90deg, #2af598 0%, #009efd 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      border: none;
    }
    &:hover {
      border-bottom: 1px solid #ffffff;
    }
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 400;
    font-size: 24px;
    line-height: 28px;
    text-decoration: none;
    color: #ffffff;
  }
  &__chart {
    @media (max-width: 350px) {
      span {
        width: 130px;
      }
    }
  }
}
.scroll {
  background: rgba(3, 10, 3, 0.908);
}
</style>
