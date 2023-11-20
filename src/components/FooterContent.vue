<script setup></script>

<template>
  <div class="footer__content">
    <div class="footer__title">Newslatter</div>
    <div class="footer__subscribe">
      <input type="text" placeholder="Enter your email" />
      <span>Subscribe</span>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.footer {
  &__content {
    padding-top: 50px;
    padding-bottom: 25px;
    width: 33%;
    @media (max-width: 1085px) {
      width: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
  }

  &__title {
    font-family: 'Work Sans';
    font-style: normal;
    font-weight: 500;
    font-size: 48px;
    line-height: 56px;
    color: #ffffff;
    padding-bottom: 20px;
    @media (max-width: 768px) {
      text-align: center;
    }
  }

  &__subscribe {
    position: relative;
    width: 463px;
    @media (max-width: 495px) {
      width: 100%;
    }
    input {
      width: 100%;
      background: rgba(255, 255, 255, 0.2);
      border: 1px solid #ffffff;
      backdrop-filter: blur(10px);
      border-radius: 50px;
      padding: 24px 30px;
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 400;
      font-size: 20px;
      line-height: 23px;
      color: #ffffff;
      &::placeholder {
        color: #ffffff;
      }
      @media (max-width: 320px) {
        font-size: 15px;
      }
    }
    span {
      cursor: pointer;
      position: absolute;
      top: 15px;
      right: 10px;
      padding-right: 10px;
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 400;
      font-size: 20px;
      line-height: 23px;
      color: #ffffff;
      background: linear-gradient(90deg, #2af598 0%, #009efd 100%);
      border-radius: 50px;
      padding: 12px 24px;
      @media (max-width: 320px) {
        font-size: 15px;
      }
    }
  }
}
</style>
