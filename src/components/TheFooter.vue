<script setup>
import { reactive } from 'vue'
import FooterContent from '@/components/FooterContent.vue'
const menuItems = reactive([
  {
    title: 'Support',
    firstRow: 'About Us',
    secondRow: 'Careers',
    thirdRow: 'Blog'
  },
  {
    title: 'Useful Link',
    firstRow: 'Payment & Tax',
    secondRow: 'Team of service',
    thirdRow: 'Privaci Policy'
  },
  {
    title: 'Our Menu',
    firstRow: 'Best Product',
    secondRow: 'Category'
  },
  {
    title: 'Address',
    firstRow: 'JL. Setiabudhi No. 193 Sukasari, Bandung West Java, Indonesia',
    secondRow: 'hallo@daunku.com'
  }
])
</script>

<template>
  <footer class="footer">
    <div class="footer__container">
      <div class="footer__row">
        <FooterContent />
        <nav class="footer__menu menu">
          <ul class="menu__list">
            <li v-for="item in menuItems" :key="item.title" class="menu__item">
              <a href="" class="menu__link">
                <div class="menu__title">{{ item.title }}</div>
              </a>
              <ul class="menu__sub-list">
                <li class="menu__sub__item">
                  <a href="" class="menu__sub-link">{{ item.firstRow }}</a>
                </li>
                <li class="menu__sub__item">
                  <a href="" class="menu__sub-link">{{ item.secondRow }}</a>
                </li>
                <li class="menu__sub__item">
                  <a href="" class="menu__sub-link">{{ item.thirdRow }}</a>
                </li>
              </ul>
            </li>
          </ul>
        </nav>
      </div>
      <div class="footer__bottom">
        <div class="footer__bottom-title">© 2022 Daunku - All rights reserved.</div>
      </div>
    </div>
  </footer>
</template>
<style lang="scss" scoped>
.footer {
  background: linear-gradient(93.99deg, #566270 0.51%, #283444 100%);
  &__container {
    max-width: 1400px;
    margin: 0 auto;
    overflow: hidden;
    padding: 0 10px;
  }
  &__row {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding-bottom: 30px;
    @media (max-width: 1325px) {
      flex-wrap: wrap;
      flex-direction: column;
      gap: 10px;
    }
  }

  &__menu {
  }
}
.menu {
  &__list {
    padding-top: 30px;
    display: flex;
    justify-content: center;
    gap: 56px;

    @media (max-width: 768px) {
      flex-wrap: wrap;
      gap: 35px;
    }
  }
  &__item {
    @media (max-width: 320px) {
      &:last-child {
        text-align: center;
      }
    }
  }
  &__link {
    text-decoration: none;
  }
  &__title {
    padding-bottom: 33px;
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 700;
    font-size: 20px;
    line-height: 140%;
    color: #ffffff;
    @media (max-width: 768px) {
      padding-bottom: 15px;
    }
  }
  &__sub-list {
    display: flex;
    flex-direction: column;
    gap: 15px;
    justify-content: center;
  }
  &__sub__item {
    max-width: 290px;
  }
  &__sub-link {
    &:hover {
      border-bottom: 1px solid #fff;
      padding-bottom: 2px;
    }
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 150%;
    color: #ffffff;
    text-decoration: none;
  }
}
.footer__bottom {
  padding: 50px 0;
  border-top: 1px solid #ffffff;
  &-title {
    text-align: center;
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 400;
    font-size: 24px;
    line-height: 28px;
    color: #ffffff;
    @media (max-width: 375px) {
      font-size: 16px;
    }
  }
}
</style>
