<script setup>
defineProps({
  type: Boolean,
});
</script>

<template>
  <section>
    <table class="card__table" v-if="type">
      <thead class="card__table-header">
        <tr class="card__table-row">
          <th class="card__table-header-item">Товар</th>
          <th class="card__table-header-item">Описание</th>
          <th class="card__table-header-item">Комментарий</th>
          <th class="card__table-header-item">Количество</th>
          <th class="card__table-header-item">Цена</th>
        </tr>
      </thead>
      <tbody class="card__table-body">
        <tr class="card__table-row" v-for="_ in 20">
          <td class="card__product-name">
            <div class="card__product-wrapper">
              <button class="card__delete">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="20"
                  height="20"
                  viewBox="0 0 20 20"
                  fill="none"
                >
                  <path
                    d="M0.189743 0.391988L0.283446 0.283446C0.62702 -0.0601288 1.16465 -0.0913545 1.5435 0.189743L1.65204 0.283446L10 8.63097L18.348 0.283446C18.7259 -0.0944772 19.3386 -0.0944772 19.7165 0.283446C20.0945 0.661369 20.0945 1.27412 19.7165 1.65204L11.369 10L19.7165 18.348C20.0601 18.6915 20.0914 19.2292 19.8102 19.608L19.7165 19.7165C19.373 20.0601 18.8354 20.0914 18.4565 19.8102L18.348 19.7165L10 11.369L1.65204 19.7165C1.27412 20.0945 0.661369 20.0945 0.283446 19.7165C-0.0944772 19.3386 -0.0944772 18.7259 0.283446 18.348L8.63097 10L0.283446 1.65204C-0.0601288 1.30847 -0.0913545 0.77084 0.189743 0.391988Z"
                    fill="#212121"
                  />
                </svg>
              </button>
              <span class="card__product-name--span">
                Шаровый гидравлический кран
              </span>
            </div>
          </td>
          <td class="card__product-description">
            <ul class="card__description-list">
              <li class="card__description-item">
                <span class="card__description-label">Артикул:</span>
                KHB-M16
              </li>
              <li class="card__description-item">
                <span class="card__description-label">Материал:</span>
                Нержавеющая сталь
              </li>
            </ul>
          </td>
          <td class="card__comment">
            <textarea
              class="card__comment-input"
              placeholder="Максимум знаков: 150"
              maxlength="150"
            ></textarea>
          </td>
          <td class="card__counter">
            <div class="card__counter-button">
              <UiCounter></UiCounter>
            </div>
          </td>
          <td class="card__sum">
            <span> 500 ₽ </span>
          </td>
        </tr>
      </tbody>
    </table>
    <table class="card__table" v-if="!type">
      <thead class="card__table-header">
        <tr class="card__table-row">
          <th class="card__table-header-item">Товар</th>
          <th class="card__table-header-item">Описание</th>
          <th class="card__table-header-item">Комментарий</th>
          <th class="card__table-header-item">Количество</th>
          <th class="card__table-header-item">Цена</th>
          <th class="card__table-header-item">Купить</th>
        </tr>
      </thead>
      <tbody class="card__table-body">
        <tr class="card__table-row" v-for="_ in 20">
          <td class="card__product-name">
            <div class="card__product-wrapper">
              <button class="card__delete">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="20"
                  height="20"
                  viewBox="0 0 20 20"
                  fill="none"
                >
                  <path
                    d="M0.189743 0.391988L0.283446 0.283446C0.62702 -0.0601288 1.16465 -0.0913545 1.5435 0.189743L1.65204 0.283446L10 8.63097L18.348 0.283446C18.7259 -0.0944772 19.3386 -0.0944772 19.7165 0.283446C20.0945 0.661369 20.0945 1.27412 19.7165 1.65204L11.369 10L19.7165 18.348C20.0601 18.6915 20.0914 19.2292 19.8102 19.608L19.7165 19.7165C19.373 20.0601 18.8354 20.0914 18.4565 19.8102L18.348 19.7165L10 11.369L1.65204 19.7165C1.27412 20.0945 0.661369 20.0945 0.283446 19.7165C-0.0944772 19.3386 -0.0944772 18.7259 0.283446 18.348L8.63097 10L0.283446 1.65204C-0.0601288 1.30847 -0.0913545 0.77084 0.189743 0.391988Z"
                    fill="#212121"
                  />
                </svg>
              </button>
              <span class="card__product-name--span">
                Шаровый гидравлический кран
              </span>
            </div>
          </td>
          <td class="card__product-description">
            <ul class="card__description-list">
              <li class="card__description-item">
                <span class="card__description-label">Артикул:</span>
                KHB-M16
              </li>
              <li class="card__description-item">
                <span class="card__description-label">Материал:</span>
                Нержавеющая сталь
              </li>
            </ul>
          </td>
          <td class="card__comment">
            <textarea
              class="card__comment-input"
              placeholder="Максимум знаков: 150"
              maxlength="150"
            ></textarea>
          </td>
          <td class="card__counter">
            <div class="card__counter-button">
              <UiCounter></UiCounter>
            </div>
          </td>
          <td class="card__sum">
            <span> 500 ₽ </span>
          </td>
          <td class="card__sum">
            <UiButtonSendButton>Добавить в корзину</UiButtonSendButton>
          </td>
        </tr>
      </tbody>
    </table>

    <div class="card__mobile">
      <div class="card__mobile-list" v-for="_ in 5">
        <div class="card__mobile-list-header">Артикул: <b>KHB-M16</b></div>
        <div class="card__mobile-list-content">
          <h3 class="card__mobile-list-content-title">
            Шаровый гидравлический кран PN 500 DN 6 M16*5
          </h3>
          <ul class="card__mobile-list-content-list">
            <li class="card__mobile-list-content-list-item">
              <span>Материал: </span><b>Нержавеющая сталь</b>
            </li>
          </ul>
        </div>
        <div class="card__mobile-list-footer">
          <div class="card__mobile-list-footer-price">Цена: <b>500 ₽</b></div>
          <div class="card__mobile-list-footer-action">
            <UiCounter></UiCounter>
            <button class="card__mobile-list-footer-action-button">
              <UiIconComents :isActive="true"></UiIconComents>
            </button>
            <button class="card__mobile-list-footer-action-button">
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
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
section {
  flex-grow: 1;
}
.card__mobile {
  display: flex;
  flex-direction: column;
  gap: 10px;

  &-list {
    border: 1px solid #d9d9d9;
    background: #f7f7f7;
    padding: 10px;
    &-footer {
      margin-top: 15px;
      &-action {
        margin-top: 15px;
        display: flex;
        gap: 10px;
        &-button {
          padding: 10px;
          background: #fff;
          border-radius: 3px;
        }
      }
      &-price {
        color: #000;
        font-family: "Myriad Pro";
        font-size: 16px;
        font-style: normal;
        font-weight: 400;
        line-height: 100%;
        & b {
          color: #000;
          text-align: center;
          font-family: "Myriad Pro";
          font-size: 18px;
          font-style: normal;
          font-weight: 600;
          line-height: 90%;
          text-transform: uppercase;
        }
      }
    }
    &-content {
      &-list {
        margin-top: 10px;
        color: #000;
        font-family: "Myriad Pro";
        font-size: 16px;
        font-style: normal;
        font-weight: 400;
        line-height: 100%;
        & b {
          color: #000;
          font-family: "Myriad Pro";
          font-size: 18px;
          font-style: normal;
          font-weight: 400;
          line-height: 90%;
        }
      }
      &-title {
        margin-top: 15px;
        color: #000;
        font-family: "Myriad Pro";
        font-size: 24px;
        font-style: normal;
        font-weight: 400;
        line-height: 100%; /* 24px */
        max-width: 326px;
      }
    }
    &-header {
      color: #000;
      font-family: "Myriad Pro";
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
      & b {
        color: #000;
        text-align: center;
        font-family: "Myriad Pro";
        font-size: 16px;
        font-style: normal;
        font-weight: 600;
        line-height: 90%;
        text-transform: uppercase;
      }
    }
  }
}

.card {
  margin-bottom: 20px;
  &__summary {
    padding: 20px;
    border: 1px solid #d9d9d9;
  }
  &__total {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 38px;
    font-style: normal;
    font-weight: 600;
    line-height: 100%;
    display: flex;
    justify-content: space-between;
    margin-bottom: 10px;
  }
  &__subtotal {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    display: flex;
    justify-content: space-between;
    margin-bottom: 20px;
  }
  &__clear-button {
    margin-top: 20px;
    color: #3064c7;
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
    border-bottom: 1px solid #3064c7;
    padding: 2px;
    background-color: #fff;
    cursor: pointer;
  }
  &__auth-link {
    color: #3064c7;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
  }
  &__auth-message {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    padding: 20px;
    border: 1px solid #d9d9d9;
  }
  &__block {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
  &__section {
    display: flex;
    gap: 20px;
  }
  &__second {
    &-subtitle {
      color: #000;
      font-family: "Myriad Pro";
      font-size: 20px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
      margin-bottom: 20px;
    }
    &-title {
      color: #000;
      font-family: "Myriad Pro";
      font-size: 40px;
      font-style: normal;
      font-weight: 400;
      line-height: 90%;
      margin-bottom: 10px;
    }
    & {
      display: flex;
      justify-content: center;
      padding-top: 329px;
      padding-bottom: 329px;
    }
    &-block {
      display: flex;
      flex-direction: column;
      align-items: center;
    }
  }
  &__second-button {
    text-transform: none;
    width: max-content !important;
    font-size: 18px;
  }
  & {
    padding-top: 30px;
  }
  &__comment {
    height: 100%;
    border: 1px solid #d9d9d9;
    padding: 10px;
    &-input {
      width: 100%;
      height: 100%;
      border: none;
      outline: none;
      display: flex;
      align-items: flex-end;
      box-sizing: border-box;
      resize: none;
      overflow-y: hidden;
      background-color: transparent;
    }
  }
  &__title {
    color: #000;
    font-family: "Century Gothic";
    font-size: 105px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    text-transform: uppercase;
  }
  &__header {
    display: flex;
    justify-content: space-between;
    padding-bottom: 30px;
    align-items: flex-end;
  }
  &__byer-button {
    width: max-content;
  }
  &__buyer {
    padding: 10px;
  }
  &__sum span {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  &__sum {
    padding: 10px;
  }

  &__counter {
    padding: 10px;
  }
  &__description-list {
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
  &__description-item {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
  }
  &__description-label {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
    opacity: 0.4;
  }
  &__product-name--span {
    width: 100%;
    text-align: center;
    color: #000;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    padding: 10px 20px;
    display: flex;
    align-items: center;
  }
  &__buyer {
    border: 1px solid #d9d9d9;
  }
  &__sum {
    border: 1px solid #d9d9d9;
  }
  &__counter-button {
    display: flex;
    justify-content: center;
  }
  &__counter {
    border: 1px solid #d9d9d9;
  }
  &__product-description {
    padding: 10px 20px;
    border: 1px solid #d9d9d9;
  }
  &__product-name {
    max-width: 520px;
    border: 1px solid #d9d9d9;
  }
  &__table-header-item {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
    padding: 17px;
    border: 1px solid #d9d9d9;
  }
  &__delete {
    cursor: pointer;
    background-color: white;
    padding: 33px 21px;
    border-right: 1px solid #d9d9d9;
  }
  &__table-body {
    height: 100px;
    border: 1px solid #d9d9d9;
  }
  &__table-header {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
  }

  &__table {
    width: 100%;
    height: 100%;
    background-color: white;
    border-collapse: collapse;
    border: 1px solid #d9d9d9;
  }
  &__product-wrapper {
    display: flex;
    height: 100%;
    align-items: center;
    & * {
      height: 100%;
    }
  }
}
.card__mobile {
  display: none;
}

@media screen and (max-width: 1439.99px) {
  .card__product-description {
    padding: 10px 10px;
    border: 1px solid #d9d9d9;
  }
}

@media screen and (max-width: 1199.99px) {
  .card__product-name--span {
    font-size: 17px;
  }
  .card__table {
    width: 100%;
    height: 100%;
    background-color: white;
    border-collapse: collapse;
    border: 1px solid #d9d9d9;
    overflow-x: auto;
    min-width: max-content;
  }
}

@media screen and (max-width: 991.99px) {
  .card__product-name--span {
    font-size: 17px;
  }
}

@media screen and (max-width: 767.99px) {
  .card__table {
    display: none;
  }
  .card__mobile {
    display: flex;
  }
}

@media screen and (max-width: 539.99px) {
}

@media screen and (max-width: 424.99px) {
}

@media screen and (max-width: 375.99px) {
}

@media screen and (max-width: 319.99px) {
}
</style>
