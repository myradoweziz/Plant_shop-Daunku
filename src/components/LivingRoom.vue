<script setup></script>

<template>
  <section class="room">
    <div class="room__contianer">
      <div class="room__row">
        <div class="room__content">
          <div class="room__title">Interior Plant Reference</div>
          <div class="room__desc">make your home so comfortable with refreshing plants</div>
        </div>
        <div class="room__image-boxex">
          <div class="room__couch">
            <div class="room__couch-image">
              <img src="../assets/img/wooden.png" alt="" />
              <span>living room</span>
              <div class="back"></div>
            </div>
            <img src="../assets/img/angle.png" alt="" />
          </div>
          <div class="room__desk">
            <img src="../assets/img/unsplash.png" alt="" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
  .room {
    padding-bottom: 100px;
    &__contianer {
      max-width: 1400px;
      margin: 0 auto;
      overflow: hidden;
      padding: 0 10px;
    }
    &__row {
    }
    &__content {
      text-align: center;
      padding-bottom: 30px;
    }
    &__title {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 500;
      font-size: 64px;
      line-height: 75px;
      color: #081323;
      padding-bottom: 5px;
      @media (max-width: 425px) {
        font-size: 50px;
        line-height: 60px;
      }
      @media (max-width: 320px) {
        font-size: 25px;
      }
    }
    &__desc {
      font-family: 'Work Sans';
      font-style: normal;
      font-weight: 400;
      font-size: 24px;
      line-height: 28px;
      color: #4f4f4f;
      @media (max-width: 375px) {
        font-size: 17px;
      }
    }
    &__image-boxex {
      display: flex;
      justify-content: space-between;
      gap: 32px;
      @media (max-width: 768px) {
        flex-wrap: wrap;
      }
    }
    &__couch {
      position: relative;
      width: 100%;
      height: 100%;
      display: flex;
      align-items: center;
      flex-direction: column;
      gap: 60px;
      transition: 0.5s all ease;
      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: center;
      }
    }
    &__couch-image {
      background: rgba(0, 0, 0, 0.3);
      border-radius: 50px;
      width: 100%;
      height: 100%;
      overflow: hidden;
      transition: 0.5s all ease;
      cursor: pointer;
      transform: scale(1, 1);
      .back {
        transition: 0.5s all ease;
        border-radius: 50px;
        opacity: 0.2;
        position: absolute;
        top: 0%;
        left: 0;
        opacity: 0.5;
        width: 100%;
        height: 100%;
      }
      &:hover {
        transition: 0.5s all ease;
        img {
          transition: 0.5s;
          transform: scale(2, 2);
        }
        .back {
          position: absolute;
          transition: 0.5s all ease;
          top: 0%;
          left: 0;
          background-color: #4f4f4f;
        }
        span {
          z-index: 3;
          transition: 0.3s all ease-in-out;
          top: 45%;
        }
      }
      span {
        font-family: 'Work Sans';
        font-style: normal;
        font-weight: 600;
        font-size: 64px;
        text-align: center;
        line-height: 75px;
        color: #ffffff;
        position: absolute;
        top: -100%;
        left: 0;
        width: 100%;
        height: 100%;
        @media (max-width: 768px) {
          font-size: 40px;
          top: 20%;
        }
        @media (max-width: 320px) {
          font-size: 35px;
          top: 15%;
        }
      }
    }
    &__desk {
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
</style>
