<template>
  <section class="favorites container" v-if="hasItems">
    <div class="favorites__header">
      <h2 class="favorites__title">Избранное</h2>
      <button class="favorites__clear-button">Очистить избранное</button>
    </div>

    <div class="favorites__section">
      <UiTableTable2 :type="false"></UiTableTable2>
    </div>

    <button class="favorites__clear-button-mob">Очистить избранное</button>
  </section>
  <section class="favorites__second container" v-else>
    <div class="favorites__second-block">
      <h2 class="favorites__second-title">Вы не добавили ни одного товара</h2>
      <span class="favorites__second-subtitle">
        Подберите интересующие вас товары в разделе каталог
      </span>
      <UiButtonSendButton class="favorites__second-button"
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

<style lang="scss">
.favorites {
  &__clear-button-mob{
    display: none;
  }
  &__section {
    overflow-x: auto;
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
    padding-bottom: 30px;
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
  &__clear-button {
    color: #3064c7;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    background-color: white;
    max-width: 216px;
    max-height: 24px;
    cursor: pointer;
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
    flex-wrap: wrap;
    gap: 20px;
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
}

@media screen and (max-width: 1439.99px) {
  .privacy-policy__header{
    margin-top: 30px;
    margin-bottom: 70px;
    display: flex;
    gap: 5px;
}
}

@media screen and (max-width: 1199.99px) {
}

@media screen and (max-width: 991.99px) {
  .favorites__title {
    color: #000;
    font-family: "Century Gothic";
    font-size: 69px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    text-transform: uppercase;
  }
  

}

@media screen and (max-width: 767.99px) {
  .favorites__clear-button {
    display: none;
    &-mob {
      display: block;
      margin-top: 20px;
      border-radius: 2px;
      border: 1px solid #d9d9d9;
      background: #fff;
      width: 100%;
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 16px;
      font-style: normal;
      font-weight: 600;
      line-height: 100%; /* 16px */
      text-transform: uppercase;
      padding: 15px;
    }
  }
}

@media screen and (max-width: 539.99px) {
  .favorites__title {
    color: #000;
    font-family: "Century Gothic";
    font-size: 56px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    text-transform: uppercase;
  }
}

@media screen and (max-width: 424.99px) {
}

@media screen and (max-width: 375.99px) {
  .favorites__title {
    font-size: 38px;
  }
}

@media screen and (max-width: 319.99px) {
}
</style>
