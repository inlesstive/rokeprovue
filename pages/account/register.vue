<script setup lang="ts">
const route = useRoute()
</script>

<template>

<section class="register container">

  <div class="register-content_block">

    <div class="first_block">
      <h2 class="title">
        Регистрация
      </h2>
    </div>

    <div class="second_block">
      <div class="placeholders">
            <input class="input" type="text" placeholder="Название компании*">
            <input class="input" type="text" placeholder="Электронная почта*">
            <input class="input" type="text" placeholder="Пароль*">
            <input class="input" type="text" placeholder="Подтвердить пароль*">
            <input class="input" type="text" placeholder="Мобильный телефон*">
            <input class="input" type="text" placeholder="Рабочий телефон*">
            <input class="input" type="text" placeholder="ИНН*">
        </div>

        <div class="politcal"> 
            <UiButtonCheckBox></UiButtonCheckBox>

            <p class="political-documentation">
              Я даю согласие на обработку персональных данных и подтверждаю, что ознакомлен с
              <a class="link" href="">политикой конфиденциальности</a> и <a class="link" href="">соглашением</a>
            </p>
          </div>

          <UiButtonSendButton>Зарегистрироваться</UiButtonSendButton>
          
        </div>

  </div>


</section>

</template>

<style lang="scss" scoped>
.first_block{
  display: flex;
  flex-basis: 50%;
}

.second_block{
  display: flex;
  flex-direction: column;
  flex-basis: 50%;
}

.title{
  color: #000;
  font-family: "Century Gothic";
  font-size: 105px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%; 
  text-transform: uppercase;
} 

.political-documentation{
  width: 763px;
  color: #808080;
  font-family: "Myriad Pro";
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%; 
  & .link{
    color: #3064C7;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    text-decoration-line: underline;
  }
}


.politcal{
  margin: 30px 0px;
  display: flex;
  gap: 9px;
}

.register-content_block{
  display: flex;
  padding: 30px 0px;
}

.placeholders{
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  grid-gap: 20px;
  margin-bottom: 20px;
}

.input{
  color: v#808080;
  font-family: "Myriad Pro";
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%;
  width: 100%;
  height: 100%;
  display: flex;
  padding: 10px 0px;
  outline: none;
  border: none;
  border-bottom: 1px solid #D9D9D9;
  &:nth-child(7){
    grid-column: 1 / -1;
  }
}

</style>