<script setup>




</script>

<template>
  <div class="auth">
    <h3 class="auth__title">Авторизация</h3>
    <div class="dv">
      <input type="text" class="auth__input" placeholder="Электронная почта*" />
      <input type="text" class="auth__input" placeholder="Пароль*" />
    </div>
    <div class="auht__wrap">
      <button class="auth__wrap-button-login">Войти</button>
      <button class="auth__wrap-button-forgot">Забыли пароль?</button>
    </div>
    <NuxtLink class="auth__link" to="/account/register">
      Зарегистрироваться
    </NuxtLink>
  </div>
</template>

<style lang="scss" scoped>
.auth {
  padding: 30px;
  background: #fff;
  display: flex;
  flex-direction: column;
  max-width: 510px;
  width: 100%;
  border: 1px solid #d9d9da;
  gap: 30px;
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
        width: 200px;
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
}
</style>
