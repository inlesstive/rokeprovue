<template>
  <div class="profile__section">
    <div class="profile__section profile__section--personal-info">
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

    <div class="profile__section profile__section--password-change">
      <span class="profile__section-title">Смена пароля</span>
      <div class="profile__inputs-grid--full">
        <input
          type="text"
          class="profile__input"
          placeholder="Текущий пароль*"
        />
        <input type="text" class="profile__input" placeholder="Новый пароль*" />
        <input
          type="text"
          class="profile__input"
          placeholder="Подтверждение пароля*"
        />
      </div>
    </div>
    <UiButtonSendButton class="profile__save-button"
      >Сохранить изменения</UiButtonSendButton
    >
  </div>
</template>

<style lang="scss" scoped>
.profile {
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
    flex-basis: 49.5%;
    display: flex;
    gap: 26px;
    flex-direction: column;
  }
  &__section--password-change {
    flex-grow: 1;
    margin-bottom: 24px;
  }
}

@media screen and (max-width: 991.99px) {
  .profile {
    &__input {
      font-size: 13px;
    }
  }
}
@media screen and (max-width: 767.99px) {
  .profile {
    &__input {
      font-size: 12px;
    }
  }
}

@media screen and (max-width: 424.99px) {
  .profile {
    &__section {
      margin-top: 20px;
      flex-basis: 100%;
      gap: 10px;
    }
    &__inputs-grid {
      display: grid;
      grid-template-columns: repeat(1, minmax(0, 1fr));
      grid-gap: 20px;
      margin-bottom: 20px;
    }
    &__inputs-grid--full {
      display: grid;
      grid-template-columns: repeat(1 minmax(0, 1fr));
      grid-gap: 20px;
      margin-bottom: 20px;
    }
    &__section-title {
      color: #000;
      font-family: "Myriad Pro";
      font-size: 20px;
      font-style: normal;
      font-weight: 600;
      line-height: 90%;
      text-transform: uppercase;
      margin-bottom: unset;
    }
    &__input {
      color: #808080;
      font-family: "Myriad Pro";
      font-size: 18px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%; /* 18px */
      width: 100%;
      height: 100%;
      display: flex;
      align-items: start;
      outline: none;
      border: none;
      border-bottom: 1px solid #d9d9d9;
      margin-bottom: 15px;
    }
    &__section--password-change {
      flex-grow: 1;
      margin-bottom: unset;
    }
  }
  .profile__section {
    margin-top: 9px;
    flex-basis: 100%;
    gap: 10px;
  }
  .profile__inputs-grid {
    grid-gap: 15px;
  }
  .profile__section.profile__section--password-change {
    margin-top: 0px;
  }
  .profile__inputs-grid--full {
    grid-gap: 15px;
  }
}

@media screen and (max-width: 375.99px) {
  .profile {
    &__inputs-grid--full {
      display: grid;
      grid-template-columns: repeat(1 minmax(0, 1fr));
      grid-gap: 20px;
      margin-bottom: 20px;
    }
    &__section-title {
      color: #000;
      font-family: "Myriad Pro";
      font-size: 20px;
      font-style: normal;
      font-weight: 600;
      line-height: 90%;
      text-transform: uppercase;
      margin-bottom: unset;
    }
    &__section--password-change {
      flex-grow: 1;
      margin-bottom: unset;
    }
  }
}
</style>
