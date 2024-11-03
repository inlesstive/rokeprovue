<template>
    <section class="profile container">
      <h2 class="profile__title" >
        {{ pageTitle }}
      </h2>
  
      <div class="profile__block">
        <div class="profile__navigation">
          <ul class="profile__menu">
            <li class="profile__menu-item">
              <UiButtonProfileButton :class="`contacts__tab-button ${currentTab === 'profile' ? 'contacts__tab-button--active' : ''}`"
                @click="setTab('profile')">Личные данные</UiButtonProfileButton>
            </li>
            <li class="profile__menu-item">
              <UiButtonProfileButton :class="`contacts__tab-button ${currentTab === 'orders' ? 'contacts__tab-button--active' : ''}`"
                @click="setTab('orders')">История заказов</UiButtonProfileButton>
            </li>
            <li class="profile__menu-item">
              <UiButtonProfileButton :class="`contacts__tab-button ${currentTab === 'favorites' ? 'contacts__tab-button--active' : ''}`"
                @click="setTab('favorites')">Избранное</UiButtonProfileButton>
            </li>
            <li class="profile__menu-item">
              <UiButtonProfileButton :class="`contacts__tab-button ${currentTab === 'details' ? 'contacts__tab-button--active' : ''}`"
                @click="setTab('details')">Реквизиты</UiButtonProfileButton>
            </li>
          </ul>
  
          <span class="profile__logout">Выйти из личного кабинета</span>
        </div>
  
        <div class="profile__content">
          <div class="profile__section profile__section--personal-info" v-if="currentTab === 'profile'">
            <span class="profile__section-title">Ваши данные</span>
            <div class="profile__inputs-grid">
              <input type="text" class="profile__input" placeholder="Полное фирменное наименование*">
              <input type="text" class="profile__input" placeholder="ИНН*">
              <input type="text" class="profile__input" placeholder="Электронная почта*">
              <input type="text" class="profile__input" placeholder="Телефон*">
            </div>
          </div>
  
          <div class="profile__section profile__section--password-change" v-if="currentTab === 'profile'">
            <span class="profile__section-title">Смена пароля</span>
            <div class="profile__inputs-grid--full">
              <input type="text" class="profile__input" placeholder="Текущий пароль*">
              <input type="text" class="profile__input" placeholder="Новый пароль*">
              <input type="text" class="profile__input" placeholder="Подтверждение пароля*">
            </div>
          </div>
          <UiButtonSendButton class="profile__save-button" v-if="currentTab === 'profile'">Сохранить изменения</UiButtonSendButton>
  
          <div v-if="currentTab === 'orders'" class="profile__section">
            <UiButtonAccordion> 23 февраля 2024
                <UiButtonAccordionItem>
                    <div>

                    </div>

                    <div>
                        <span>
                            Товаров на сумму: 1 500 000 ₽
                        </span>
                    </div>
                </UiButtonAccordionItem>
            </UiButtonAccordion>
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
  import { ref } from 'vue';
  
  const currentTab = ref('profile'); // Установите начальную вкладку на "profile"
  
  const setTab = (tab) => {
    currentTab.value = tab; // Устанавливает активную вкладку
    console.log('Активная вкладка:', tab); // Логирование активной вкладки для отладки
  };

  const pageTitle = computed(() => {
  switch (currentTab.value) {
    case 'orders':
      return 'История заказов';
    case 'favorites':
      return 'Избранное';
    case 'details':
      return 'Реквизиты';
    default:
      return 'Профиль пользователя';
  }
});
</script>
  
  

<style lang="scss" scoped>
.profile{
    &__logout{
        color:#17172D;
        font-family: "Myriad Pro";
        font-size: 20px;
        font-style: normal;
        font-weight: 400;
        line-height: 100%;
    }
    &__block{
        display: flex;
    }
    &__title{
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
    &__navigation{
        display: flex;
        flex-basis: 50%;
        gap: 30px ;
        flex-direction: column;

    }
    &__content{
        flex-basis: 50%;
        display: flex;
        flex-direction: column;
    }
    &__inputs-grid{
        display: grid;
        grid-template-columns: repeat(2, minmax(0, 1fr));
        grid-gap: 20px;
        margin-bottom: 26px;
    }
    &__inputs-grid--full{
        display: grid;
        grid-template-columns: repeat(1 minmax(0, 1fr));
        grid-gap: 20px;
    }
    &__input{
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
    &__section-title{
        color: #000;
        font-family: "Myriad Pro";
        font-size: 20px;
        font-style: normal;
        font-weight: 600;
        line-height: 90%; 
        text-transform: uppercase;
        margin-bottom: 26px;
    }
    &__section{
        display: flex;
        gap: 26px;
        flex-direction: column;
    }
    &__section--password-change{
        margin-bottom: 24px;
    }
    &__block{
        margin-bottom: 30px;
    }
}
</style>