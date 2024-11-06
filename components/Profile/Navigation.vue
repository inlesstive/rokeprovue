<template>
  <div class="profile__navigation">
    <ul class="profile__menu">
      <li class="profile__menu-item">
        <NuxtLink to="/account/personaldata">
          <UiButtonProfileButton
            :class="`contacts__tab-button ${
              $route.path === '/account/personaldata'
                ? 'contacts__tab-button--active'
                : ''
            }`"
          >
            Личные данные
          </UiButtonProfileButton>
        </NuxtLink>
      </li>
      <li class="profile__menu-item">
        <NuxtLink to="/account/orders">
          <UiButtonProfileButton
            :class="`contacts__tab-button ${
              $route.path === '/account/orders'
                ? 'contacts__tab-button--active'
                : ''
            }`"
          >
            История заказов
          </UiButtonProfileButton>
        </NuxtLink>
      </li>
      <li class="profile__menu-item">
        <NuxtLink to="/account/favorites">
          <UiButtonProfileButton
            :class="`contacts__tab-button ${
              $route.path === '/account/favorites'
                ? 'contacts__tab-button--active'
                : ''
            }`"
          >
            Избранное
          </UiButtonProfileButton>
        </NuxtLink>
      </li>
      <li class="profile__menu-item">
        <NuxtLink to="/account/details">
          <UiButtonProfileButton
            :class="`contacts__tab-button ${
              $route.path === '/account/details'
                ? 'contacts__tab-button--active'
                : ''
            }`"
          >
            Реквизиты
          </UiButtonProfileButton>
        </NuxtLink>
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
</script>

<style lang="scss" scoped>
.contacts__tab-button--active {
  background: #3064c7;
  color: white;
}

.profile {
  &__navigation {
    display: flex;
    flex-basis: 35%;
    gap: 30px;
    flex-direction: column;
  }
}
@media screen and (max-width: 767.99px) {
  .profile {
    &__navigation {
      display: none;
      flex-basis: 20%;
      gap: 30px;
      flex-direction: column;
    }
  }
}
</style>
