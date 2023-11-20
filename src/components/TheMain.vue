<script setup>
  import BaseIcon from './BaseIcon.vue'
</script>

<template>
  <main class="place">
    <div class="place__wrapper">
      <div class="place__bg_img">
        <img src="../assets/img/main_img.png" alt="" />
      </div>
      <div class="place__container">
        <div class="place__content">
          <div class="place__title">
            Bring Serenity to Your Place <br />
            With Interior Plants
          </div>
          <div class="place__desc">
            find your dream plant for you home decoration <br />
            with us, and we will make it happen.
            <BaseIcon name="point" />
          </div>
          <div class="place__search">
            <input type="text" placeholder="Search plant" />
            <BaseIcon name="search" />
          </div>
          <div class="place__points">
            <BaseIcon name="point" />
            <div class="place__count_point">
              <div class="place__count">
                <span>
                  <p>$65.00</p>
                  Dracena Fragnas
                </span>
              </div>
              <BaseIcon class="count-point" name="point" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
  .place {
    padding-bottom: 100px;
    width: 100%;
    height: 100%;
    &__wrapper {
      display: flex;
      align-items: center;
      flex-direction: column;
      position: relative;
      width: 100%;
      height: 100vh;
      @media (max-width: 425px) {
        height: 100%;
      }
    }
    &__container {
      padding: 0 10px;
      padding-top: 150px;
      max-width: 1400px;
      margin: 0 auto;
      @media (max-width: 850px) {
        padding-top: 87px;
      }
    }
    &__bg_img {
      position: absolute;
      top: 0;
      left: 0;
      z-index: -1;
      width: 100%;
      height: 100vh;
      overflow: hidden;
      @media (max-width: 425px) {
        height: 100%;
      }
      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: center;
      }
    }
    &__content {
      text-align: center;
      padding: 0 5px;
      @media (max-width: 425px) {
        padding: 10px 5px;
      }
    }
    &__title {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 700;
      font-size: 82px;
      text-align: center;
      line-height: 96px;
      color: #ffffff;
      padding-bottom: 20px;
      @media (max-width: 850px) {
        br {
          display: none;
        }
        font-size: 70px;
        line-height: 86px;
      }
      @media (max-width: 550px) {
        font-size: 50px;
        line-height: 76px;
      }
      @media (max-width: 470px) {
        font-size: 30px;
        line-height: 50px;
      }
    }
    &__desc {
      position: relative;
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 400;
      font-size: 24px;
      line-height: 150%;
      color: #ffffff;
      padding-bottom: 20px;
      span {
        position: absolute;
        top: -25px;
        left: -310px;
      }
      @media (max-width: 550px) {
        font-size: 16px;
      }
    }
    &__search {
      position: relative;
      width: 463px;
      text-align: center;
      display: inline-block;
      padding-bottom: 10px;
      @media (max-width: 495px) {
        width: 100%;
      }
      input {
        background: rgba(255, 255, 255, 0.2);
        border: 1px solid #ffffff;
        backdrop-filter: blur(10px);
        border-radius: 50px;
        width: 100%;
        padding: 24px;
        font-family: 'Work Sans';
        font-style: normal;
        font-weight: 400;
        font-size: 20px;
        line-height: 23px;
        color: #ffffff;
        @media (max-width: 425px) {
          padding: 12px;
        }
        &:focus {
          border: 1px solid #ffffff;
          outline: none;
        }
        &::placeholder {
          font-family: 'Work Sans';
          font-style: normal;
          font-weight: 400;
          font-size: 20px;
          line-height: 23px;
          color: #ffffff;
          @media (max-width: 425px) {
            font-size: 16px;
          }
        }
      }
      span {
        cursor: pointer;
        position: absolute;
        top: 13px;
        right: 0px;
        padding-right: 10px;
        @media (max-width: 425px) {
          top: 0;
          width: 50px;
          height: 50px;
        }
      }
    }
    &__points {
      display: flex;
      align-items: center;
      justify-content: space-between;
      width: 100%;
      padding-top: 10px;
      position: relative;
    }
    &__count_point {
      display: flex;
      align-items: center;
      flex-direction: column;
      &:hover {
        .place__count {
          display: block;
        }
      }
    }
    &__count {
      display: none;
      position: absolute;
      top: -110px;
      right: 0px;
      transform: translateX(50%);
      background: rgba(255, 255, 255, 0.2);
      border: 1px solid #ffffff;
      backdrop-filter: blur(5px);
      border-radius: 24px;
      padding: 20px;
      margin-bottom: 30px;
      p {
        font-family: 'Work Sans';
        font-style: normal;
        font-weight: 700;
        font-size: 32px;
        line-height: 38px;
        color: #ffffff;
        margin: 0;
        padding-bottom: 5px;
      }
      span {
        font-family: 'Work Sans';
        font-style: normal;
        font-weight: 700;
        font-size: 16px;
        line-height: 19px;
        color: #ffffff;
      }
    }
  }
  .count-point {
    cursor: pointer;
  }
</style>
