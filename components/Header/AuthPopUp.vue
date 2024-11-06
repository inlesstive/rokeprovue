<script setup>
const toggleMode = ref(true);
</script>

<template>
  <div class="auth" @click="$emit('popupclose')">
    <div class="auth__flex" @click.stop v-if="toggleMode">
      <h3 class="auth__title">Авторизация</h3>
      <div class="dv">
        <input
          type="text"
          class="auth__input"
          placeholder="Электронная почта*"
        />
        <input type="text" class="auth__input" placeholder="Пароль*" />
      </div>
      <div class="auht__wrap">
        <button class="auth__wrap-button-login">Войти</button>
        <button
          class="auth__wrap-button-forgot"
          @click="toggleMode = !toggleMode"
        >
          Забыли пароль?
        </button>
      </div>
      <NuxtLink class="auth__link" to="/account/register">
        Зарегистрироваться
      </NuxtLink>
    </div>

    <div class="auth__flex" @click.stop v-if="!toggleMode">
      <h3 class="auth__title">Запрос пароля</h3>
      <p class="auth__text">
        Введите электронную почту, указанную при регистрации
      </p>
      <div class="dv">
        <input
          type="text"
          class="auth__input"
          placeholder="Электронная почта*"
        />
      </div>
      <div class="auht__wrap">
        <button class="auth__wrap-button-login">Запросить пароль</button>
        <button
          class="auth__wrap-button-forgot"
          @click="toggleMode = !toggleMode"
        >
          Помню пароль!
        </button>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.auth {
  background: #fff;
  display: flex;
  flex-direction: column;
  max-width: 510px;
  width: 100%;
  border: 1px solid #d9d9d9;
  border-top: 0;
  gap: 30px;
  &__flex {
    display: flex;
    flex-direction: column;
    gap: 30px;
    background: #fff;
    padding: 30px;
    margin: 0 20px;
  }
  &__link {
    color: #3064c7;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%; /* 24px */
  }
  &__wrap {
    margin-top: 30px;
    &-button {
      &-forgot {
        color: #3064c7;
        background: transparent;
        /* Кнопка 1 */
        font-family: "Myriad Pro";
        font-size: 18px;
        font-style: normal;
        font-weight: 600;
        line-height: 90%; /* 16.2px */
        margin-left: 20px;
        cursor: pointer;
      }
      &-login {
        border-radius: 3px;
        background: #3064c7;
        padding: 20px;
        color: #fff;
        font-family: "Myriad Pro";
        font-size: 24px;
        font-style: normal;
        font-weight: 400;
        line-height: 100%;
        cursor: pointer;
      }
    }
  }
  &__input {
    color: #808080;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    padding: 10px 0;
    border: 0;
    border-bottom: 1px solid #d9d9d9;
    outline: none;
    width: 100%;
    &::placeholder {
      color: #808080;
      font-family: "Myriad Pro";
      font-size: 24px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
    }
  }
  &__title {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 40px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
  }
  &__text {
    color: #17172d;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
  }
}

@media screen and (max-width: 1439.99px) {
}

@media screen and (max-width: 1199.99px) {
}

@media screen and (max-width: 991.99px) {
}

@media screen and (max-width: 767.99px) {
  .header__popup {
    position: fixed;
    right: 0;
    top: 0;
    z-index: 1000;
    background: #0000006c;
    width: 100vw !important;
    height: 100vh;
    max-width: 100%;
    justify-content: center;
  }
}

@media screen and (max-width: 539.99px) {
}

@media screen and (max-width: 424.99px) {
}

@media screen and (max-width: 375.99px) {
}

@media screen and (max-width: 319.99px) {
}
</style>
