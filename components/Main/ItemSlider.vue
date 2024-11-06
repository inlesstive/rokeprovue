<template>
  <div class="itemslider">
    <NuxtImg src="http://localhost:3000/image/item_slider-4.png" />
    <div class="itemslider-info">
      <h3 class="itemslider-info-subtitle">/Инфраструктура и строительство</h3>
      <div class="itemslider-info-wrapper">
        <h2 class="itemslider-info-title">
          Надежность и качество на долгие годы вперед
        </h2>
        <p class="itemslider-info-descr">
          Наша продукция является надежной основой для инфраструктурных и
          строительных проектов. Обладая высоким уровнем качества и
          безопасности.
        </p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.itemslider {
  position: relative;
  & img {
    width: 100%;
    max-height: auto;
    object-fit: cover;
  }
  &-info {
    position: absolute;
    bottom: 20px;
    right: 20px;
    background: white;
    max-width: 530px;
    padding: 20px;
    display: flex;
    flex-direction: column;
    gap: 20px;
    &-wrapper {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }

    &-descr {
      color: #808080;
      font-family: "Myriad Pro";
      font-size: 20px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
    }
    &-title {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 40px;
      font-style: normal;
      font-weight: 400;
      line-height: 90%;
    }
    &-subtitle {
      color: #808080;

      font-family: "Myriad Pro";
      font-size: 20px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
    }
  }
}

@media screen and (max-width: 1439.99px) {
  .itemslider-info-subtitle {
    font-size: 18px;
  }
  .itemslider-info-title {
    font-size: 36px;
  }
  .itemslider-info-descr {
    color: #808080;
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
  }
  .itemslider-info {
    max-width: 470px;
    padding: 15px;
  }
}

@media screen and (max-width: 1199.99px) {
  .itemslider img {
    width: 100%;
    max-height: 566px;
    -o-object-fit: cover;
    object-fit: cover;
  }
  .itemslider-info-subtitle {
    font-size: 20px;
  }
  .itemslider-info-title {
    font-size: 40px;
  }
  .itemslider-info-descr {
    color: #808080;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
  }
  .itemslider-info {
    max-width: 560px;
    padding: 15px;
  }
}

@media screen and (max-width: 991.99px) {
}

@media screen and (max-width: 767.99px) {
  .itemslider-info {
    position: unset;
  }
  .itemslider img {
    width: 160px;
  }
  .itemslider {
    background: #f7f7f7;
    padding: 10px;
  }
  .itemslider-info {
    background: unset;
    padding: 0;
    margin-top: 10px;
    max-width: 100%;
  }
}

@media screen and (max-width: 539.99px) {
  .itemslider img {
    width: 131px;
  }
  .itemslider-info-title {
    font-size: 24px;
  }
  .itemslider-info-subtitle {
    font-size: 10px;
  }
  .itemslider-info-descr {
    font-size: 16px;
  }
  .itemslider-info {
    gap: 10px;
  }
}

@media screen and (max-width: 424.99px) {
}

@media screen and (max-width: 375.99px) {
  .itemslider img {
    width: 131px !important;
    height: 70px !important;
  }
  .itemslider-info {
    margin-top: 6px;
  }
  .itemslider-info-wrapper {
    gap: 12px;
  }
}

@media screen and (max-width: 319.99px) {
}
</style>
