<template>
  <section class="card container" v-if="hasItems">
    <div class="card__header">
      <h2 class="card__title">Корзина</h2>
    </div>

    <div class="card__section">
      <UiTableTable2></UiTableTable2>
      <div class="card__block">
        <div class="card__summary">
          <h3 class="card__total">
            Итого
            <span class="card__total-amount">1 000 ₽</span>
          </h3>
          <h4 class="card__subtotal">
            Товаров на сумму
            <span class="card__subtotal-amount">1 000 ₽</span>
          </h4>

          <UiButtonSendButton class="card__checkout-button"
            >Перейти к оформлению</UiButtonSendButton
          >

          <button class="card__clear-button">Очистить корзину</button>
        </div>

        <span class="card__auth-message"
          >Для управления заказами необходима
          <a href="" class="card__auth-link">авторизация</a></span
        >
      </div>
    </div>
  </section>
  <section class="card__second container" v-else>
    <div class="card__second-block">
      <h2 class="card__second-title">Вы не добавили ни одного товара</h2>
      <span class="card__second-subtitle">
        Подберите интересующие вас товары в корзину
      </span>
      <UiButtonSendButton class="card__second-button"
        >Перейти в каталог</UiButtonSendButton
      >
    </div>
  </section>
</template>

<script lang="ts">
import { UiButtonSendButton } from "#build/components";

export default {
  setup() {
    const hasItems = ref(true);

    return {
      hasItems,
    };
  },
};
</script>

<style lang="scss" scoped>
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
@media screen and (max-width: 1439.99px) {
}

@media screen and (max-width: 1199.99px) {
  .card__block {
    display: flex;
    flex-direction: column;
    gap: 10px;
    position: fixed;
    background: #fff;
    width: 100%;
    bottom: 0;
    left: 0;
    box-shadow: 0px -4px 3px 0px rgba(0, 0, 0, 0.2);
    padding: 20px;
  }
  .card__section {
    overflow-x: auto;
  }
  .card__second-title {
    text-align: center;
  }
  .card__second-subtitle {
    text-align: center;
  }
}

@media screen and (max-width: 991.99px) {
}

@media screen and (max-width: 767.99px) {
  .card__auth-message {
    font-size: 20px;
    & a {
      font-size: 20px;
    }
  }
}

@media screen and (max-width: 539.99px) {
  .card__title {
    font-size: 67px;
  }
}

@media screen and (max-width: 424.99px) {
}

@media screen and (max-width: 375.99px) {
}

@media screen and (max-width: 319.99px) {
}
</style>
