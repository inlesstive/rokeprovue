<script setup lang="ts">
import { ref } from "vue";

const breadcrumbsData = [
  { text: "Главная", to: "/" },
  { text: "Каталог", to: "/" },
  { text: "Запорная арматура", to: "/catalog/valves/123" },
  { text: "Высокого давления", to: "/catalog/valves/high-pressure" },
  { text: "Квадратный корпус", to: "/catalog/valves/high-pressure/kvadratiny" },
];

const list = ref([
  { id: 1, name: "asdasd", quantity: 1, cost: 500 },
  { id: 2, name: "asdasd", quantity: 1, cost: 500 },
  { id: 3, name: "asdasd", quantity: 1, cost: 500 },
]);

const isOpen = ref(false);

const activeTabs = ref("desc");
</script>

<template>
  <div class="product container">
    <UiBreadCrumbs :crumbs="breadcrumbsData"></UiBreadCrumbs>

    <Swiper class="swiper" :slides-per-view="1" :loop="true">
      <SwiperSlide v-for="slide in 10" :key="slide">
        <div class="product__side-image">
          <NuxtImg src="http://localhost:3000/image/main_hits-img.png" />
        </div>
      </SwiperSlide>
    </Swiper>
    <div class="product__side-wrapper">
      <div class="product__side flex-basic-1">
        <div class="product__side-images">
          <div class="product__side-image" v-for="_ in 3">
            <NuxtImg src="http://localhost:3000/image/main_hits-img.png" />
          </div>
        </div>
      </div>
      <div class="product__side flex-basic-2">
        <h1 class="product__side-title">
          2х ходовой шаровый кран высокого давления
        </h1>
        <div class="product__side-price">500 руб.</div>
        <div class="product__side-wrap">
          <ul class="product__side-wrapper-info">
            <li class="product__side-wrapper-info-item" v-for="_ in 5">
              <span class="product__side-wrapper-info-item-name">Артикул</span>
              <span class="product__side-wrapper-info-item-value">KHB-M16</span>
            </li>
          </ul>
          <div class="product__side-wrapper-action">
            <div class="product__side-wrapper-action-head">
              <UiButtonSendButton>Добавить в корзину</UiButtonSendButton>
              <button class="product__side-wrapper-action-head-button">
                <UiIconComents :is-active="true"></UiIconComents>
              </button>
              <button class="product__side-wrapper-action-head-button">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="34"
                  height="30"
                  viewBox="0 0 34 30"
                  fill="none"
                >
                  <path
                    d="M18.39 2.73611L16.9951 4.16302L15.5957 2.73482C12.028 -0.906693 6.24355 -0.906693 2.67582 2.73482C-0.891939 6.37632 -0.891939 12.2804 2.67582 15.9219L16.0954 29.6189C16.5932 30.127 17.4004 30.127 17.8983 29.6189L31.3281 15.9193C34.888 12.2658 34.8941 6.37828 31.3258 2.73611C27.7515 -0.912036 21.9642 -0.912036 18.39 2.73611Z"
                    fill="#3064C7"
                  />
                </svg>
              </button>
            </div>
            <div class="product__side-wrapper-action-bottom">
              <p>Остатки по складам</p>
              <div>
                <span>Центральный склад</span>
                <span>100 шт.</span>
              </div>
            </div>
          </div>
        </div>
        <div class="product__side-tabs">
          <div class="product__side-tabs-selector">
            <button
              :class="`product__side-tabs-selector-button ${
                activeTabs === 'desc' ? 'active' : ''
              }`"
              @click="activeTabs = 'desc'"
            >
              Описание
            </button>
            <button
              :class="`product__side-tabs-selector-button ${
                activeTabs === 'table' ? 'active' : ''
              }`"
              @click="activeTabs = 'table'"
            >
              Характеристики
            </button>
          </div>
          <div class="product__side-tabs-content" v-if="activeTabs == 'desc'">
            <p>
              Lorem ipsum, dolor sit amet consectetur adipisicing elit.
              Repellendus debitis ab quidem, necessitatibus doloremque quam est.
              Quisquam dolores possimus, harum optio eum voluptatibus voluptates
              autem veniam laudantium illum quia magnam.
            </p>
          </div>

          <div class="product__side-tabs-content" v-if="activeTabs == 'table'">
            <div class="product__side-tabs-content-flex">
              <span>Технические характеристики</span>
              <button>Скачать PDF файл</button>
            </div>

            <div class="product__side-tabs-content-table" v-for="_ in 0">
              <NuxtImg src="http://localhost:3000/image/scheme.png" />
              <div class="product__side-tabs-content-table-wrap">
                <table>
                  <thead>
                    <tr>
                      <th rowspan="2">Артикул для заказа</th>
                      <th rowspan="2">PN</th>
                      <th rowspan="2">DN</th>
                      <th colspan="10">РАЗМЕРЫ (мм)</th>
                    </tr>
                    <tr>
                      <th>D1</th>
                      <th>D2</th>
                      <th>DM</th>
                      <th>L</th>
                      <th>L1</th>
                      <th>L2</th>
                      <th>L3</th>
                      <th>H1</th>
                      <th>H2</th>
                      <th>B</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr v-for="_ in 8">
                      <td>KHB-M16</td>
                      <td>500</td>
                      <td>06</td>
                      <td>6</td>
                      <td>11</td>
                      <td>M16*1.5</td>
                      <td>69</td>
                      <td>40</td>
                      <td>11</td>
                      <td>1,4</td>
                      <td>32</td>
                      <td>13</td>
                      <td>26</td>
                    </tr>
                  </tbody>
                </table>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="product__similar" v-if="false">
      <h3 class="product__similar-title">похожие товары</h3>

      <UiTable></UiTable>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.flex-basic-1 {
  flex-basis: 45%;
}
.flex-basic-2 {
  flex-basis: 55%;
}
table {
  border-collapse: collapse;
  border: 1px solid #d7d7d7;
  & th {
    color: var(---, #17172d);
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 600;
    line-height: 90%;
    padding: 9px;
  }
  & td {
    padding: 10px;
    color: var(---, #17172d);
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
  }
  & td,
  th {
    text-align: center;
    border: 1px solid #d7d7d7;
  }
}

.product {
  // .product__side-wrapper
  margin-top: 15px;
  margin-bottom: 60px;
  &__similar {
    margin-top: 150px;

    &-title {
      color: #17172d;
      font-family: "Century Gothic";
      font-size: 60px;
      font-style: normal;
      font-weight: 700;
      line-height: 90%;
      letter-spacing: -1.2px;
      text-transform: uppercase;
      margin-bottom: 30px;
    }
  }

  &__side-wrapper {
    display: flex;
    justify-content: space-between;
    margin-top: 15px;
    gap: 20px;
  }

  // .product__side
  &__side-wrap {
    display: flex;
    gap: 20px;
  }

  &__side {
  }

  // .product__side-images

  &__side-images {
    display: flex;
    flex-direction: column;
    gap: 20px;
    & img {
      max-width: 573px;
    }
  }

  // .product__side-image

  &__side-image {
    display: flex;
    justify-content: center;
    align-items: center;
    background: #f7f7f7;
  }

  // .product__side-title

  &__side-title {
    color: #17172d;
    font-family: "Century Gothic";
    font-size: 70px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    letter-spacing: -1.4px;
    text-transform: uppercase;
  }

  // .product__side-price

  &__side-price {
    margin-top: 20px;
    color: #17172d;
    font-family: "Myriad Pro";
    font-size: 38px;
    font-style: normal;
    font-weight: 600;
    line-height: 100%;
    text-transform: uppercase;
  }

  // .product__side-wrapper-info

  &__side-wrapper-info {
    flex-basis: 50%;
  }

  // .product__side-wrapper-info-item

  &__side-wrapper-info-item {
    display: flex;
    justify-content: space-between;
    border-top: 1px solid #d7d7d7;
    padding: 10px 0;
    &:last-child {
      border-bottom: 1px solid #d7d7d7;
    }
  }

  // .product__side-wrapper-info-item-name

  &__side-wrapper-info-item-name {
    color: #17172d;
    opacity: 0.4;
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
  }

  // .product__side-wrapper-info-item-value

  &__side-wrapper-info-item-value {
    color: var(---, #17172d);

    /* Текст 2 */
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%; /* 20px */
  }

  // .product__side-wrapper-action

  &__side-wrapper-action {
    flex-basis: 50%;
    background: #f7f7f7;
    height: max-content;
    padding: 20px;
  }

  // .product__side-wrapper-action-head

  &__side-wrapper-action-head {
    display: flex;
    gap: 10px;
    &-button {
      padding: 12px;
      border-radius: 3px;
      background: #fff;
      cursor: pointer;
    }
  }

  // .product__side-wrapper-action-bottom

  &__side-wrapper-action-bottom {
    & p {
      color: #17172d;
      margin-top: 21px;

      font-family: "Myriad Pro";
      font-size: 24px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%; /* 24px */
    }
    & div {
      display: flex;
      justify-content: space-between;
      margin-top: 10px;
      & span {
        color: #17172d;
        font-family: "Myriad Pro";
        font-size: 18px;
        font-style: normal;
        font-weight: 400;
        line-height: 90%;
        opacity: 0.3;
      }
    }
  }

  // .product__side-tabs

  &__side-tabs {
  }

  // .product__side-tabs-selector

  &__side-tabs-selector {
    margin-top: 60px;
    display: flex;
  }

  // .product__side-tabs-selector-button

  &__side-tabs-selector-button {
    background: transparent;
    color: #17172d;
    font-family: "Myriad Pro";
    font-size: 25px;
    font-style: normal;
    font-weight: 600;
    line-height: 100%;
    text-transform: uppercase;
    padding: 10px;
    cursor: pointer;
    border-bottom: 2px solid #d9d9d9;
    transition: 0.2s;
    &:hover {
      color: #3976e7;
      border-bottom: 2px solid #3976e7;
    }
    &.active {
      color: #3064c7;
      border-bottom: 2px solid #3064c7;
    }
  }

  // .product__side-tabs-content

  &__side-tabs-content {
    margin-top: 40px;
  }

  // .product__side-tabs-content-flex

  &__side-tabs-content-flex {
    display: flex;
    justify-content: space-between;
    & span {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 30px;
      font-style: normal;
      font-weight: 400;
      line-height: 90%; /* 27px */
    }
    & button {
      display: inline-flex;
      padding: 10px 15px;
      justify-content: center;
      align-items: center;
      gap: 10px;
      color: #fff;
      font-family: "Myriad Pro";
      font-size: 18px;
      font-style: normal;
      font-weight: 600;
      line-height: 90%;
      border-radius: 3px;
      cursor: pointer;
      background: #3064c7;
    }
  }

  // .product__side-tabs-content-table

  &__side-tabs-content-table {
    margin-top: 30px;
    display: flex;
    & img {
      flex-grow: 1;
      border: 1px solid #d7d7d7;
      border-right: 0px;
      height: auto;
      object-fit: contain;
      padding: 45px;
    }
  }
}
.swiper {
  margin-top: 20px;
}

@media screen and (max-width: 1439.99px) {
  .product__side-title {
    color: #17172d;
    font-family: "Century Gothic";
    font-size: 62px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    letter-spacing: -1.4px;
    text-transform: uppercase;
  }
  .product__side-wrap {
    display: flex;
    gap: 20px;
    flex-direction: column;
  }
  .product__side-tabs-content-table img {
    display: none;
  }
}

@media screen and (max-width: 1199.99px) {
  .product__side-tabs-content-table {
    display: block;
    overflow-x: auto; /* Добавляет горизонтальную прокрутку при необходимости */
    -webkit-overflow-scrolling: touch; /* Плавная прокрутка для мобильных устройств */
    width: 100%; /* Ширина контейнера соответствует ширине родителя */
  }
  table {
    width: 100%;
  }
}

@media screen and (max-width: 991.99px) {
  .flex-basic-1 {
    display: none;
  }
  .flex-basic-2 {
    flex-basis: unset;
  }
}

@media screen and (max-width: 767.99px) {
  .product__side:first-child {
    display: none;
  }

  .product__side-tabs-content-table-wrap {
    overflow-x: auto;
  }

  table {
    min-width: 1000px; /* Минимальная ширина таблицы для активации прокрутки */
    width: auto; /* Таблица займет минимально необходимую ширину */
  }
  .product__side-title {
    color: #17172d;
    font-family: "Century Gothic";
    font-size: 52px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    letter-spacing: -1.4px;
    text-transform: uppercase;
  }
  .product__side-tabs-selector-button.active {
    color: #3064c7;
    flex-grow: 1;
    border: 2px solid #3064c7;
  }
  .product__side-tabs-selector {
    gap: 15px;
  }
  .product__side-tabs-selector-button {
    border: 2px solid #d9d9d9;
    flex-grow: 1;
    &:hover {
      border: 2px solid #3064c7;
    }
  }
  .product__side-slider {
    margin-bottom: 20px;
    & img {
      max-height: 500px;
      background: #f7f7f7;
      object-fit: contain;
    }
  }
}

@media screen and (max-width: 539.99px) {
  .product__side-title {
    color: #17172d;
    font-family: "Century Gothic";
    font-size: 45px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    letter-spacing: -1.4px;
    text-transform: uppercase;
  }
  .product__side-tabs-selector {
    margin-top: 60px;
    display: flex;
    flex-wrap: wrap;
    width: 100%;
  }
}

@media screen and (max-width: 424.99px) {
}

@media screen and (max-width: 375.99px) {
}

@media screen and (max-width: 319.99px) {
}
</style>
