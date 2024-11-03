<script setup lang="ts">
const route = useRoute();
</script>

<template>
  <section class="news container">
    <h1 class="news__title">
      <div class="news__title-position">
        <span class="news__subtitle">Актуальные события</span><br />
        и новинки от&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ROKE
      </div>

      <div class="news__title--mobile">
        <span class="news__subtitle--mobile">Актуальные <br />события</span> ROKE
      </div>
    </h1>

    <div class="news__cards">
      <div class="news__card" v-for="_ in 2">
        <div class="news__card-item">
          <span class="news__card-date">15.08.2024</span>

          <img class="news__card-image" src="/public/image/news2.png" alt="" />

          <div class="news__card-description">
            <span class="news__card-title">Получение сертификата DNV</span>

            <p class="news__card-info">
              Наша компания получила сертификат DNV, что подтверждает
              соответствие продукции требованиям стандарта для морских судов и
              оборудования.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>


<style lang="scss" scoped>
.news {
  padding-top: 30px;
  padding-bottom: 30px;
  &__subtitle--mobile{
    color: #3064C7;
      font-family: "Century Gothic";
      font-size: 40px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%; 
      letter-spacing: -0.8px;
      text-transform: uppercase;
  }

  &__title--mobile{
    display: none;
    color: #000;
      font-family: "Century Gothic";
      font-size: 40px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%;
      letter-spacing: -0.8px;
      text-transform: uppercase;
  }
  &__title {
    width: max-content;
    position: relative;

    &-position {
      color: var(---, #17172d);
      font-family: "Century Gothic";
      font-size: 105px;
      font-style: normal;
      font-weight: 700;
      line-height: 90%;
      text-transform: uppercase;
    }

    &-mob {
      display: none;
    }

    &::before {
      width: 182px;
      height: 12px;
      content: "";
      background: #17172d;
      position: absolute;
      right: 280px;
      bottom: 7px;
    }
  }

  &__subtitle {
    color: var(---, #3064c7);
    font-family: "Century Gothic";
    font-size: 105px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    text-transform: uppercase;
  }

  &__cards {
    margin-top: 60px;
    display: grid;
    gap: 20px;
    grid-template-columns: repeat(3, minmax(0, 1fr));
  }

  &__card {
    background: #f7f7f7;
    display: inline-flex;
    height: auto;
    padding: 20px;
    flex-direction: column;
    align-items: flex-start;
    gap: 10px;
    flex-shrink: 0;
    border: 1px solid #d9d9d9;

    &-item {
      display: flex;
      width: 100%;
      flex-direction: column;
      justify-content: space-between;
      align-items: flex-start;
      gap: 20px;

      & img {
        width: 100%;
      }
    }
  }

  &__description {
    display: flex;
    width: 85%;
    flex-direction: column;
    gap: 10px;
  }

  &__date {
    color: #808080;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
  }

  &__card-title {
    color: #17172d;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 600;
    line-height: 90%;
    text-transform: uppercase;
  }

  &__card-info {
    color: #808080;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
  }

  @media screen and (max-width: 1439.99px) {
    &__title {
      &-position {
        font-size: 85px;
      }
    }

    &__title--mob {
      display: none;
    }

    &__subtitle {
      font-size: 85px;
    }

    &__cards {
      grid-template-columns: repeat(2, minmax(0, 1fr));
    }

    &__title::before {
      width: 160px;
      right: 220px;
      bottom: 5px;
    }
  }

  @media screen and (max-width: 1199.99px) {
    &__title--mob {
      display: none;
    }

    &__title {
      &-position {
        font-size: 65px;
      }
    }

    &__subtitle {
      font-size: 65px;
    }

    &__title::before {
      width: 120px;
      right: 170px;
      bottom: 4px;
    }
  }

  @media screen and (max-width: 991.99px) {
    &__card-title {
      font-size: 15px;
    }

    &__card-info {
      font-size: 15px;
    }

    &__date {
      font-size: 15px;
    }

    &__title {
      &-mob {
        display: none;
      }

      &-position {
        font-size: 55px;
      }
    }

    &__subtitle {
      font-size: 55px;
    }

    &__title::before {
      height: 8px;
      width: 105px;
      right: 141px;
      bottom: 3px;
    }
  }

  @media screen and (max-width: 767.99px) {
    &__subtitle--mobile{
      font-size: 70px;
    }

    &__title--mobile{
    display: block;
    font-size: 70px;
   }

    &__title-position {
      display: none;
    }

    &__card-title {
      font-size: 12px;
    }

    &__card-info {
      font-size: 13px;
    }

    &__date {
      font-size: 14px;
    }

    &__title-position {
      display: none;
    }

    &__title {
      color: #000;
      font-family: "Century Gothic";
      font-size: 60px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%;
      letter-spacing: -0.8px;
      text-transform: uppercase;
    }

    &__title::before {
      display: none;
    }

    &__subtitle {
      display: none !important;
    }

    &__title--mob {
      display: block;

      & span {
        color: #3064c7;
        font-family: "Century Gothic";
        font-size: 60px;
        font-style: normal;
        font-weight: 700;
        line-height: 100%;
        letter-spacing: -0.8px;
        text-transform: uppercase;
      }
    }
  }

  @media screen and (max-width: 539.99px) {
    &__subtitle--mobile{
      font-size: 50px;
    }

    &__title--mobile{
    display: block;
    font-size: 50px;
   }

    &__title-position {
      display: none;
    }

    &__title {
      color: #000;
      font-family: "Century Gothic";
      font-size: 40px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%;
      letter-spacing: -0.8px;
      text-transform: uppercase;
    }

    &__subtitle {
      color: #3064c7;
      font-family: "Century Gothic";
      font-size: 40px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%;
      letter-spacing: -0.8px;
      text-transform: uppercase;
    }

    &__title::before {
      display: none;
    }

    &__cards {
      gap: 10px;
      margin-top: 10px;
      grid-template-columns: repeat(1, minmax(0, 1fr));
    }

    &__card {
      display: flex;
      width: 100%;
      padding: 10px;
      flex-direction: column;
      gap: 5px;
    }

    &__date {
      font-size: 10px;
    }

    &__card-item img {
      max-width: 218px;
    }

    &__card-item {
      display: flex;
      gap: 10px;
      width: auto;
    }

    &__card-title {
      font-size: 17px;
    }

    &__card-info {
      width: auto;
      font-size: 16px;
    }

    &__description {
      width: auto;
      display: flex;
      gap: 5px;
    }

    &__title--mob {
      & span {
        color: #3064c7;
        font-family: "Century Gothic";
        font-size: 40px;
        font-style: normal;
        font-weight: 700;
        line-height: 100%;
        letter-spacing: -0.8px;
        text-transform: uppercase;
      }
    }
  }

  @media screen and (max-width: 375.99px) {
    &__subtitle--mobile{
      font-size: 40px;
    }

    &__title--mobile{
    display: block;
    font-size: 40px;
   }

    &__title-position {
      display: none;
    }

    &__title {
      color: #000;
      font-family: "Century Gothic";
      font-size: 40px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%;
      letter-spacing: -0.8px;
      text-transform: uppercase;
    }

    &__subtitle {
      color: #3064c7;
      font-family: "Century Gothic";
      font-size: 40px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%;
      letter-spacing: -0.8px;
      text-transform: uppercase;
    }

    &__title::before {
      display: none;
    }

    &__cards {
      gap: 10px;
      margin-top: 10px;
      grid-template-columns: repeat(1, minmax(0, 1fr));
    }

    &__card {
      display: flex;
      width: 100%;
      padding: 10px;
      flex-direction: column;
      gap: 5px;
    }

    &__date {
      font-size: 10px;
    }

    &__card-item img {
      max-width: 218px;
    }

    &__card-item {
      display: flex;
      gap: 10px;
      width: auto;
    }

    &__card-title {
      font-size: 17px;
    }

    &__card-info {
      width: auto;
      font-size: 16px;
    }

    &__description {
      width: auto;
      display: flex;
      gap: 5px;
    }


    &__title--mob {
      & span {
        color: #3064c7;
        font-family: "Century Gothic";
        font-size: 40px;
        font-style: normal;
        font-weight: 700;
        line-height: 100%;
        letter-spacing: -0.8px;
        text-transform: uppercase;
      }
    }
  }
}
</style>

