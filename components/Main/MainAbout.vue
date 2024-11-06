<script setup lang="ts"></script>

<template>
  <section class="mainabout container">
    <div class="mainabout__top">
      <h3 class="mainabout__top-title">о нас</h3>
      <p class="mainabout__top-descr">
        Мы специализируемся на поставках бесшовных труб, трубных соединений,
        трубных крепежей, шаровых кранов и резьбовых соединений под одно или два
        врезных кольца. Наша продукция доступна как на наших складах в России,
        так и под заказ в любом объеме.
      </p>
    </div>
    <div class="mainabout__content">
      <div class="mainabout__content-item">
        <div class="mainabout__content-item-line"></div>
      </div>
      <div class="mainabout__content-item">
        <h4 class="mainabout__content-item-title">Лет гарантии</h4>
        <span class="mainabout__content-item-sub">5</span>
      </div>
      <div class="mainabout__content-item">
        <h4 class="mainabout__content-item-title">Лет на рынке</h4>
        <span class="mainabout__content-item-sub">11</span>
      </div>
      <div class="mainabout__content-item">
        <h4 class="mainabout__content-item-title">Продуктов</h4>
        <span class="mainabout__content-item-sub">50 000 +</span>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.mainabout {
  &__content {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    &-item {
      padding: 20px;
      border-top: 1px solid #d7d7d7;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      min-height: 380px;

      &-line {
        position: relative;
        width: 100%;
        height: 100%;
        &::after {
          content: "";
          position: absolute;
          width: 100%;
          height: 1px;
          background-color: #d7d7d7;
          height: 1px;
          transform: rotate(-20deg);
          bottom: 170px;
        }
      }

      &:nth-child(2) {
        border-left: 1px solid #d7d7d7;
      }
      &:nth-child(4) {
        border-left: 1px solid #d7d7d7;
      }
      &-title {
        color: #808080;
        font-family: "Myriad Pro";
        font-size: 24px;
        font-style: normal;
        font-weight: 400;
        line-height: 100%;
      }
      &-sub {
        color: #17172d;

        font-family: "Century Gothic";
        font-size: 220px;
        font-style: normal;
        font-weight: 700;
        line-height: 80%;
        letter-spacing: -6.6px;
        text-transform: uppercase;
      }
    }
  }
  &__top {
    display: flex;

    padding-bottom: 30px;
    &-title {
      color: #17172d;

      font-family: "Century Gothic";
      font-size: 16px;
      font-style: normal;
      font-weight: 700;
      line-height: 90%;
      text-transform: uppercase;
    }
    &-descr {
      color: #17172d;

      max-width: 501px;
      font-family: "Myriad Pro";
      font-size: 20px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
    }
    & * {
      flex-basis: 50%;
    }
  }
}

@media screen and (max-width: 1439.99px) {
  .mainabout__content-item-sub {
    font-size: 124px;
  }
}

@media screen and (max-width: 1199.99px) {
  .mainabout__content-item {
    min-height: 295px;
  }
  .mainabout__content-item-sub {
    font-size: 119px;
  }
  .mainabout__content-item-line::after {
    transform: rotate(-26deg);
    bottom: 133px;
  }
}

@media screen and (max-width: 991.99px) {
  .mainabout__content-item-sub {
    font-size: 87px;
  }
}

@media screen and (max-width: 767.99px) {
  .mainabout__content-item-line::after {
    transform: rotate(-35deg);
    bottom: 133px;
  }
  .mainabout__content-item {
    padding: 20px;
    border-top: unset;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    min-height: 380px;
  }

  .mainabout__content {
    gap: 10px;
  }

  .mainabout__content-item {
    border: 0 !important;
    border: 1px solid #d7d7d7 !important;
    min-height: 118px;
    gap: 30px;
    padding: 15px;
    &:nth-child(1) {
      display: none;
    }
    &:nth-child(2) {
      border-left: 0;
    }
    &:nth-child(4) {
      border-left: 0;
      grid-column: 1 / -1;
    }
  }
  .mainabout__top {
    display: flex;
    padding-bottom: 30px;
    flex-direction: column;
    gap: 10px;
  }
}

@media screen and (max-width: 539.99px) {
}

@media screen and (max-width: 424.99px) {
  .mainabout__top-title[data-v-47faeaab] {
    color: #17172d;
    font-family: "Century Gothic";
    font-size: 10px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    text-transform: uppercase;
  }
  .mainabout__content-item-title {
    color: #808080;
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    opacity: 0.5;
  }
  .mainabout__content-item-sub {
    color: #17172d;
    font-family: "Century Gothic";
    font-size: 87px;
    font-style: normal;
    font-weight: 700;
    line-height: 80%;
    letter-spacing: -2.8px;
    text-transform: uppercase;
  }
  .mainabout__top {
    padding-bottom: 20px;
  }
  .mainabout__content-item {
    min-height: 148px;
  }
}

@media screen and (max-width: 375.99px) {
}

@media screen and (max-width: 319.99px) {
}
</style>
