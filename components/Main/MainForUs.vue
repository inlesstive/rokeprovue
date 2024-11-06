<script setup></script>

<template>
  <section class="mainforus container">
    <div class="mainforus__top">
      <span class="mainforus__top-descriptor">Для кого подойдет</span>
      <h3 class="mainforus__top-title">
        <div class="mainforus__top-title-pos">
          <span>Решения</span> для <br />
          ключевых &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; отраслей
        </div>
        <div class="mainforus__top-title-pos mob">
          <span>Решения </span>для ключевых отраслей
        </div>
      </h3>
    </div>
    <Swiper
      class="swiper-desk"
      :slides-per-view="1"
      :loop="true"
      :space-between="20"
      :breakpoints="{
        992: {
          slidesPerView: 1,
        },
        1200: {
          slidesPerView: 2,
        },
      }"
    >
      <SwiperSlide v-for="slide in 10" :key="slide">
        <MainItemSlider></MainItemSlider>
      </SwiperSlide>
      <ClientOnly>
        <div class="wrapper">
          <MainSwiperCon></MainSwiperCon>
        </div>
      </ClientOnly>
    </Swiper>
    <div class="mainforus-mob-wrapper">
      <MainItemSlider class="mob" v-for="_ in 4"></MainItemSlider>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.wrapper {
  width: 100%;
  display: flex;
  justify-content: center;
  gap: 10px;
  margin-top: 20px;
}
.mob {
  display: none;
}
.mainforus {
  padding-top: 150px;
  padding-bottom: 150px;
  &__top {
    display: flex;
    margin-bottom: 31px;
    justify-content: space-between;
    &-title {
      &-pos {
        color: #17172d;
        font-family: "Century Gothic";
        font-size: 70px;
        font-style: normal;
        font-weight: 700;
        line-height: 90%;
        letter-spacing: -1.4px;
        text-transform: uppercase;
        position: relative;
        &::after {
          content: "";
          position: absolute;
          width: 175px;
          height: 8px;
          background: #17172d;
          right: 321px;
          bottom: 5px;
        }
      }
      & span {
        color: #3064c7;

        font-family: "Century Gothic";
        font-size: 70px;
        font-style: normal;
        font-weight: 700;
        line-height: 90%;
        letter-spacing: -1.4px;
        text-transform: uppercase;
      }
    }
    &-descriptor {
      color: #17172d;

      font-family: "Century Gothic";
      font-size: 16px;
      font-style: normal;
      font-weight: 700;
      line-height: 90%;
      text-transform: uppercase;
    }
  }
}

@media screen and (max-width: 1439.99px) {
  .mainforus__top-title-pos::after {
    content: "";
    position: absolute;
    width: 160px;
    height: 8px;
    background: #17172d;
    right: 334px;
    bottom: 5px;
  }
}

@media screen and (max-width: 1199.99px) {
  .mainforus__top-title-pos {
    font-size: 56px;
    & span {
      font-size: 56px;
    }
  }
  .mainforus__top-title-pos::after {
    content: "";
    position: absolute;
    width: 127px;
    height: 7px;
    background: #17172d;
    right: 263px;
    bottom: 4px;
  }
}

@media screen and (max-width: 991.99px) {
  .mainforus__top {
    flex-direction: column;
  }
  .mainforus__top-title-pos::after {
    content: "";
    position: absolute;
    width: 127px;
    height: 7px;
    background: #17172d;
    left: 300px;
    right: unset;
    bottom: 2px;
  }
}

@media screen and (max-width: 767.99px) {
  .swiper-desk {
    display: none;
  }
  .mainforus-mob-wrapper {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
  .mob {
    display: block !important;
  }
  .mainforus__top-title-pos {
    display: none;
    margin-top: 10px;
  }
  .mainforus__top-title-pos::after {
    display: none;
  }
  .wrapper {
    display: none;
  }
}

@media screen and (max-width: 539.99px) {
  .mainforus__top-title-pos {
    font-size: 35px;
    & span {
      font-size: 35px;
    }
  }
}

@media screen and (max-width: 424.99px) {
  .mainforus__top-descriptor {
    color: #17172d;
    font-family: "Century Gothic";
    font-size: 10px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    text-transform: uppercase;
  }
  .mainforus {
    padding-top: 61px;
    padding-bottom: 68px;
  }
  .mainforus__top-title-pos {
    font-family: "Century Gothic";
    font-size: 35px;
    font-style: normal;
    font-weight: 700;
    line-height: 100%;
    letter-spacing: -0.7px;
    text-transform: uppercase;
    & span {
      font-family: "Century Gothic";
      font-size: 35px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%;
      letter-spacing: -0.7px;
      text-transform: uppercase;
    }
  }
  .mainforus__top {
    margin-bottom: 10px;
  }
}

@media screen and (max-width: 375.99px) {
}

@media screen and (max-width: 319.99px) {
}
</style>
