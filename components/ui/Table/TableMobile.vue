<template>
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
        </div>
      </div>
    </div>
  </div>
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
    margin-top: 25px;
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
</style>
