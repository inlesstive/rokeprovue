<template>
  <section class="profile container">
    <h2 class="profile__title">
      {{ pageTitle }}
    </h2>

    <div class="profile__block">
      <div class="profile__navigation">
        <ul class="profile__menu">
          <li class="profile__menu-item">
            <UiButtonProfileButton
              :class="`contacts__tab-button ${
                currentTab === 'profile' ? 'contacts__tab-button--active' : ''
              }`"
              @click="setTab('profile')"
              >Личные данные</UiButtonProfileButton
            >
          </li>
          <li class="profile__menu-item">
            <UiButtonProfileButton
              :class="`contacts__tab-button ${
                currentTab === 'orders' ? 'contacts__tab-button--active' : ''
              }`"
              @click="setTab('orders')"
              >История заказов</UiButtonProfileButton
            >
          </li>
          <li class="profile__menu-item">
            <UiButtonProfileButton
              :class="`contacts__tab-button ${
                currentTab === 'favorites' ? 'contacts__tab-button--active' : ''
              }`"
              @click="setTab('favorites')"
              >Избранное</UiButtonProfileButton
            >
          </li>
          <li class="profile__menu-item">
            <UiButtonProfileButton
              :class="`contacts__tab-button ${
                currentTab === 'details' ? 'contacts__tab-button--active' : ''
              }`"
              @click="setTab('details')"
              >Реквизиты</UiButtonProfileButton
            >
          </li>
        </ul>

        <span class="profile__logout">Выйти из личного кабинета</span>
      </div>

      <div class="profile__content">
        <div
          class="profile__section profile__section--personal-info"
          v-if="currentTab === 'profile'"
        >
          <span class="profile__section-title">Ваши данные</span>
          <div class="profile__inputs-grid">
            <input
              type="text"
              class="profile__input"
              placeholder="Полное фирменное наименование*"
            />
            <input type="text" class="profile__input" placeholder="ИНН*" />
            <input
              type="text"
              class="profile__input"
              placeholder="Электронная почта*"
            />
            <input type="text" class="profile__input" placeholder="Телефон*" />
          </div>
        </div>

        <div
          class="profile__section profile__section--password-change"
          v-if="currentTab === 'profile'"
        >
          <span class="profile__section-title">Смена пароля</span>
          <div class="profile__inputs-grid--full">
            <input
              type="text"
              class="profile__input"
              placeholder="Текущий пароль*"
            />
            <input
              type="text"
              class="profile__input"
              placeholder="Новый пароль*"
            />
            <input
              type="text"
              class="profile__input"
              placeholder="Подтверждение пароля*"
            />
          </div>
        </div>
        <UiButtonSendButton
          class="profile__save-button"
          v-if="currentTab === 'profile'"
          >Сохранить изменения</UiButtonSendButton
        >

        <div v-if="currentTab === 'orders'" class="profile__section">
          <div class="order">
            <UiButtonAccordionCabinet class="order__accordion">
              <div class="profile__section-table-wrapper" v-for="_ in 5">
                <span>23 февраля 2024</span>
                <UiButtonAccordionItemCabinet
                  class="order__item"
                  title="Свернуть"
                >
                  <table class="order__table">
                    <thead>
                      <tr>
                        <th class="order__table-header">Наименование товара</th>
                        <th class="order__table-header">Описание</th>
                        <th class="order__table-header">Количество</th>
                        <th class="order__table-header">Сумма</th>
                      </tr>
                    </thead>
                    <tbody>
                      <tr class="order__row" v-for="_ in 10">
                        <td class="order__product-name">
                          Шаровый гидравлический кран
                        </td>
                        <td class="order__product-description">
                          <ul class="order__description-list">
                            <li class="order__description-item">
                              <span class="order__description-label"
                                >Артикул:</span
                              >
                              KHB-M16
                            </li>
                            <li class="order__description-item">
                              <span class="order__description-label"
                                >Материал:</span
                              >
                              Нержавеющая сталь
                            </li>
                          </ul>
                        </td>
                        <td class="order__quantity">1 000</td>
                        <td class="order__sum">500 000 ₽</td>
                      </tr>
                    </tbody>
                  </table>
                  <div class="order__summary">
                    <span class="order__total-label"
                      >Товаров на сумму: 1 500 000 ₽</span
                    >
                    <h3 class="order__total-heading">Итого: 1 500 000 ₽</h3>
                  </div>
                </UiButtonAccordionItemCabinet>
              </div>
            </UiButtonAccordionCabinet>
          </div>
        </div>

        <div v-if="currentTab === 'favorites'" class="profile__section">
          <span class="profile__section-title">Избранное</span>
          <p>Здесь будут отображаться ваши избранные товары.</p>
        </div>

        <div v-if="currentTab === 'details'" class="profile__section">
          <span class="profile__section-title">Реквизиты</span>
          <p>Здесь вы можете добавить или изменить реквизиты.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from "vue";

const currentTab = ref("profile");

const setTab = (tab: any) => {
  currentTab.value = tab;
  console.log("Активная вкладка:", tab);
};

const pageTitle = computed(() => {
  switch (currentTab.value) {
    case "orders":
      return "История заказов";
    case "favorites":
      return "Избранное";
    case "details":
      return "Реквизиты";
    default:
      return "Профиль пользователя";
  }
});
</script>

<style lang="scss" scoped>
.profile {
  &__section-table-wrapper {
    display: flex;
    flex-direction: column;
    gap: 10px;
    & span {
      margin-left: 20px;
    }
  }
  &__logout {
    color: #17172d;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
  }
  &__block {
    display: flex;
  }
  &__title {
    color: #000;
    font-family: "Century Gothic";
    font-size: 105px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    text-transform: uppercase;
    margin-top: 30px;
    margin-bottom: 59px;
  }
  &__navigation {
    display: flex;
    flex-basis: 20%;
    gap: 30px;
    flex-direction: column;
  }
  &__content {
    flex-basis: 80%;
    display: flex;
    flex-direction: column;
  }
  &__inputs-grid {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    grid-gap: 20px;
    margin-bottom: 26px;
  }
  &__inputs-grid--full {
    display: grid;
    grid-template-columns: repeat(1 minmax(0, 1fr));
    grid-gap: 20px;
  }
  &__input {
    color: #808080;
    font-family: "Myriad Pro";
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    width: 100%;
    height: 100%;
    display: flex;
    align-items: start;
    outline: none;
    border: none;
    border-bottom: 1px solid #d9d9d9;
    margin-bottom: 30px;
  }
  &__section-title {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 600;
    line-height: 90%;
    text-transform: uppercase;
    margin-bottom: 26px;
  }
  &__section {
    display: flex;
    gap: 26px;
    flex-direction: column;
  }
  &__section--password-change {
    margin-bottom: 24px;
  }
  &__block {
    margin-bottom: 30px;
  }
}
.order {
  &__accordion {
    max-width: 1563px;
  }
  &__table {
    width: 100%;
    background-color: white;
    border-collapse: collapse;
    border: 1px solid #d9d9d9;
  }
  &__table-header {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 600;
    line-height: 90%;
    padding: 17px 20px;
    border: 1px solid #d9d9d9;
  }
  &__item {
    width: 100%;
  }
  &__product-name {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    padding: 10px 20px;
    border: 1px solid #d9d9d9;
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
  &__product-description {
    border: 1px solid #d9d9d9;
  }
  &__description-item {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
  }
  &__description-list {
    padding: 10px 20px;
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
  &__quantity {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 600;
    line-height: 90%;
    padding: 10px;
    border: 1px solid #d9d9d9;
    text-align: center;
  }
  &__sum {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    padding: 10px;
    border: 1px solid #d9d9d9;
    text-align: center;
  }
  &__summary {
    display: flex;
    justify-content: space-between;
    margin-top: 20px;
  }
  &__total-label {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
  }
  &__total-heading {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 38px;
    font-style: normal;
    font-weight: 600;
    line-height: 100%;
  }
}
</style>
