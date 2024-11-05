<template>
  <section class="profile container">
    <UiBreadCrumbs :crumbs="breadcrumbsData" class="breadcrumbs">
    </UiBreadCrumbs>
    <h2 class="profile__title">
      {{ breadcrumbsData[breadcrumbsData.length - 1].text }}
    </h2>

    <div class="profile__block profile__block-profile">
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
    </div>

    <div class="personal__account mob">
      <div class="personal__account-data mob">
        Личные данные
        <svg
          width="14"
          height="13"
          viewBox="0 0 14 13"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M1.33786 11.8686L0.969285 12.2064L0.29356 11.4693L0.662137 11.1314L1.33786 11.8686ZM12.6621 0.131423C12.8657 -0.0551739 13.182 -0.0414219 13.3686 0.162137C13.5552 0.365697 13.5414 0.681981 13.3379 0.868577L12.6621 0.131423ZM0.662137 11.1314L12.6621 0.131423L13.3379 0.868577L1.33786 11.8686L0.662137 11.1314Z"
            fill="#17172D"
          />
          <path
            d="M13 11.5L13 0.5L0.999999 0.5"
            stroke="#17172D"
            stroke-linecap="square"
            stroke-linejoin="round"
          />
        </svg>
      </div>
      <div class="personal__account-orders mob">
        История заказов
        <svg
          width="14"
          height="13"
          viewBox="0 0 14 13"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M1.33786 11.8686L0.969285 12.2064L0.29356 11.4693L0.662137 11.1314L1.33786 11.8686ZM12.6621 0.131423C12.8657 -0.0551739 13.182 -0.0414219 13.3686 0.162137C13.5552 0.365697 13.5414 0.681981 13.3379 0.868577L12.6621 0.131423ZM0.662137 11.1314L12.6621 0.131423L13.3379 0.868577L1.33786 11.8686L0.662137 11.1314Z"
            fill="#17172D"
          />
          <path
            d="M13 11.5L13 0.5L0.999999 0.5"
            stroke="#17172D"
            stroke-linecap="square"
            stroke-linejoin="round"
          />
        </svg>
      </div>
      <div class="presonal__account-elect mob">
        Избранное
        <svg
          width="14"
          height="13"
          viewBox="0 0 14 13"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M1.33786 11.8686L0.969285 12.2064L0.29356 11.4693L0.662137 11.1314L1.33786 11.8686ZM12.6621 0.131423C12.8657 -0.0551739 13.182 -0.0414219 13.3686 0.162137C13.5552 0.365697 13.5414 0.681981 13.3379 0.868577L12.6621 0.131423ZM0.662137 11.1314L12.6621 0.131423L13.3379 0.868577L1.33786 11.8686L0.662137 11.1314Z"
            fill="#17172D"
          />
          <path
            d="M13 11.5L13 0.5L0.999999 0.5"
            stroke="#17172D"
            stroke-linecap="square"
            stroke-linejoin="round"
          />
        </svg>
      </div>
      <div class="personal__account-details mob">
        Реквизиты
        <svg
          width="14"
          height="13"
          viewBox="0 0 14 13"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M1.33786 11.8686L0.969285 12.2064L0.29356 11.4693L0.662137 11.1314L1.33786 11.8686ZM12.6621 0.131423C12.8657 -0.0551739 13.182 -0.0414219 13.3686 0.162137C13.5552 0.365697 13.5414 0.681981 13.3379 0.868577L12.6621 0.131423ZM0.662137 11.1314L12.6621 0.131423L13.3379 0.868577L1.33786 11.8686L0.662137 11.1314Z"
            fill="#17172D"
          />
          <path
            d="M13 11.5L13 0.5L0.999999 0.5"
            stroke="#17172D"
            stroke-linecap="square"
            stroke-linejoin="round"
          />
        </svg>
      </div>
      <span class="profile__logout">Выйти из личного кабинета</span>
    </div>

  </section>
</template>

<script setup lang="ts">
import { ref } from "vue";

const breadcrumbsData = [
  { text: "Профиль", to: "/" },
  { text: "Личный кабинет", to: "/" },
];

const currentTab = ref("profile");

const isOpen = ref(false);

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
.mob {
  display: none;
}
.breadcrumbs {
  display: none;
}

.contacts__tab-button--active {
  background: #3064c7;
  color: white;
}
.profile {
  &__block-profile {
    justify-content: space-between;
  }

  &__first-block--content {
    flex-basis: 45% !important;
  }

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
    flex-grow: 1;
    margin-bottom: 24px;
  }
  &__block {
    margin-bottom: 30px;
  }
}

@media screen and (max-width: 375.99px) {
  .personal__account-elect{
      padding: 20px 10px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid #D9D9D9;
    }
  .personal__account{
    &{
      display: flex;
      flex-direction: column;
      margin-bottom: 99px;
    }
    &-data{
      padding: 20px 10px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-top: 1px solid #D9D9D9;
      border-bottom: 1px solid #D9D9D9;
    }
    &-details{
      padding: 20px 10px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid #D9D9D9;
      margin-bottom: 20px;
    }
    &-orders{
      padding: 20px 10px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid #D9D9D9;
    }

  }
  .mob{
    display: flex;
  }
  .profile {
    &__block {
      display: none;
    }
    &__title {
      width: 100%;
      font-size: 40px;
      margin-bottom: 20px;
      margin-top: 10px;
    }
  }
}
</style>
