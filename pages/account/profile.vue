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

        <div class="profile__section profile__section--password-change"
          v-if="currentTab === 'profile'">
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
            <table class="favorites__table">
                <thead class="favorites__table-header">
                    <tr class="favorites__table-row">
                        <th class="favorites__table-header-item">Товар</th>
                        <th class="favorites__table-header-item">Описание</th>
                        <th class="favorites__table-header-item">Количество</th>
                        <th class="favorites__table-header-item">Цена</th>
                        <th class="favorites__table-header-item">Купить</th>
                    </tr>
                </thead>
                <tbody class="favorites__table-body">
                    <tr class="favorites__table-row" v-for="_ in 3">
                        <td class="favorites__product-name">
                            <button class="favorites__delete">
                                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20" fill="none">
                                    <path d="M0.189743 0.391988L0.283446 0.283446C0.62702 -0.0601288 1.16465 -0.0913545 1.5435 0.189743L1.65204 0.283446L10 8.63097L18.348 0.283446C18.7259 -0.0944772 19.3386 -0.0944772 19.7165 0.283446C20.0945 0.661369 20.0945 1.27412 19.7165 1.65204L11.369 10L19.7165 18.348C20.0601 18.6915 20.0914 19.2292 19.8102 19.608L19.7165 19.7165C19.373 20.0601 18.8354 20.0914 18.4565 19.8102L18.348 19.7165L10 11.369L1.65204 19.7165C1.27412 20.0945 0.661369 20.0945 0.283446 19.7165C-0.0944772 19.3386 -0.0944772 18.7259 0.283446 18.348L8.63097 10L0.283446 1.65204C-0.0601288 1.30847 -0.0913545 0.77084 0.189743 0.391988Z" fill="#212121"/>
                                </svg>
                            </button>
                            <span class="favorites__product-name--span">
                                Шаровый гидравлический кран
                            </span>
                        </td>
                        <td class="favorites__product-description">
                            <ul class="favorites__description-list">
                                <li class="favorites__description-item">
                                    <span class="favorites__description-label">Артикул:</span>
                                    KHB-M16
                                </li>
                                <li class="favorites__description-item">
                                    <span class="favorites__description-label">Материал:</span>
                                    Нержавеющая сталь
                                </li>
                            </ul>
                        </td>
                        <td class="favorites__counter">
                            <div class="favorites__counter-controls">
                                <button class="favorites__counter-button" >
                                    <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 14 14" fill="none" @click="">
                                        <rect y="6" width="14" height="2" fill="black"/>
                                    </svg>
                                </button>
                                <span class="favorites__counter-value">1</span>
                                <button class="favorites__counter-button" >
                                    <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 14 14" fill="none">
                                        <rect y="6" width="14" height="2" fill="black"/>
                                        <rect x="6" y="14" width="14" height="2" transform="rotate(-90 6 14)" fill="black"/>
                                    </svg>
                                </button>
                            </div>
                        </td>
                        <td class="favorites__sum">
                            <span>
                                500 ₽
                            </span>
                        </td>
                        <td class="favorites__buyer">
                            <UiButtonSendButton class="favorites__byer-button">Добавить в корзину</UiButtonSendButton>
                        </td>
                    </tr>
                </tbody>
            </table>
        </div>


        <div v-if="currentTab === 'details'" class="profile__section">
<<<<<<< Updated upstream
            <div class="details">
                <ul class="details__list">
                    <li class="details__list-item">
                        <span class="details__message">Реквизиты не добавлены</span>
                    </li>
                    <li class="details__list-item">
                        <p class="details__description">
                            У вас пока нет сохраненных реквизитов. Добавьте <br> данные — это ускорит оформление заказа.
                        </p>
                    </li>
                    <li class="details__list-item">                            
                            <button class="details__popup-button" @click="isOpen=!isOpen"> 
                                <span>
                                    Добавить новые реквизиты
                                </span>
                            </button>
                    </li>
                </ul>
            </div>
<<<<<<< Updated upstream
            <UiModal></UiModal>
=======
          <span class="profile__section-title">Реквизиты</span>
>>>>>>> Stashed changes
=======
            <UiModal v-if="isOpen" @closeModal="closeModal"></UiModal>
>>>>>>> Stashed changes
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from "vue";

const currentTab = ref("profile");


const isOpen = ref(false)

const closeModal = () => {
    isOpen.value = false;
};

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
.details{
    &__list{
        display: flex;
        align-items: flex-start ;
        gap: 20px;
        flex-direction: column ;
    }
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
    &__message{
        color: #000;
        font-family: "Myriad Pro";
        font-size: 40px;
        font-style: normal;
        font-weight: 400;
        line-height: 90%; 
    }
    &__description{
        color: #000;
        font-family: "Myriad Pro";
        font-size: 20px;
        font-style: normal;
        font-weight: 400;
        line-height: 100%;
    }
    &__popup-button{
        padding: 10px;
        background-color: white;
        color: #000;
        text-transform: none;
        border: 1px solid #D9D9D9;
        cursor: pointer;
        font-size: 20px ;
        font-style: normal;
        font-weight: 400;
        line-height: 100%; 
        font-family: "Myriad Pro";
        transition: 0.3s ;
    }
    &__popup-button:hover{
        background-color: #3064C7;
        color: white;
    }
}

.contacts__tab-button--active{
    background: #3064C7;
    color: white;
}

.favorites{
    &__byer-button{
        max-width: 279px;
    }
    &__buyer{
        padding: 10px;
    }
    &__sum span{
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
    &__sum{
        padding: 10px;
    }
    &__counter-button{
        cursor: pointer;
        background-color: white;
    }
    &__counter-value{
        margin-left: 20px;
        margin-right: 20px;
    }
    &__counter-controls{
        border: 1px solid #D9D9D9;
        color: #000;
        font-family: "Myriad Pro";
        font-size: 20px;
        font-style: normal;
        font-weight: 600;
        line-height: 90%;
        display: flex;
        justify-content: center;
        padding: 11px 0px ;
    }
    &__counter{
        padding: 10px;
    }
    &__description-list{
        display: flex;
        flex-direction: column;
        gap: 10px;
    }
    &__description-item{
        color: #000;
        font-family: "Myriad Pro";
        font-size: 18px;
        font-style: normal;
        font-weight: 400;
        line-height: 90%;
    }
    &__description-label{
        color: #000;
        font-family: "Myriad Pro";
        font-size: 18px;
        font-style: normal;
        font-weight: 400;
        line-height: 90%; 
        opacity: 0.4;
    }
    &__product-name--span{
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
    &__buyer{
        border: 1px solid #D9D9D9;
    }
    &__sum{
        border: 1px solid #D9D9D9;
    }
    &__counter{
        border: 1px solid #D9D9D9;
    }
    &__product-description{
        padding: 10px 20px; 
        border: 1px solid #D9D9D9;
    }
    &__product-name{
        max-width: 520px;    
        border: 1px solid #D9D9D9;
    }
    &__table-header-item{
        color: #000;
        font-family: "Myriad Pro";
        font-size: 20px;
        font-style: normal;
        font-weight: 400;
        line-height: 90%; 
        padding: 17px;
        border: 1px solid #D9D9D9;
    }
    &__delete{
        cursor: pointer;
        background-color: white; 
        padding: 33px 21px;
        border-right: 1px solid #D9D9D9;
    }
    &__table-body{
        border: 1px solid #D9D9D9;
    }
    &__table-header{
    color: #000;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
    }

  &__table{
    width: 100%;
    background-color: white;
    border-collapse: collapse;
    border: 1px solid #d9d9d9;
  }
}


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
