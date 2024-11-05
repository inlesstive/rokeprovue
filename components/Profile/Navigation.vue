<template>
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
</template>

<script setup lang="ts">
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

<style lang="scss">
.contacts__tab-button--active {
  background: #3064c7;
  color: white;
}

.profile {
  &__navigation {
    display: flex;
    flex-basis: 20%;
    gap: 30px;
    flex-direction: column;
  }
}
</style>
