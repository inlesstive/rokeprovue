<script setup lang="ts">
const route = useRoute()

const tabs = ref(true)


</script>



<template>
  <section class="contact container">
    <h2 class="title">
      Контакты
    </h2>

    <div class="contact_block">
      
      <div class="contact-block_top">

        <div class="connect">

          <button :class="`contact-button ${tabs ? 'active' : ''}` " @click="tabs = true">

            <svg width="10" height="10" viewBox="0 0 10 10" fill="none" xmlns="http://www.w3.org/2000/svg">
              <rect width="10" height="10" fill="currentColor"/>
            </svg>

              Свяжитесь с нами
          </button>

        </div>

        <div class="form">

          <button :class="`contact-button ${!tabs ? 'active' : ''}` " @click="tabs = false">

          <svg width="10" height="10" viewBox="0 0 10 10" fill="none" xmlns="http://www.w3.org/2000/svg">
            <rect width="10" height="10" fill="currentColor"/>
          </svg>

            форма заявки
          </button>

        </div>

      </div>


      <div class="contact-content_block" v-if="tabs">


          <div class="first_block">
            <p class="dscr">
              Свяжитесь с нами и мы ответим<br> на вопросы
            </p>
          </div>

          <div class="second_block">
              <div class="connect-details">
                <div class="address">
                  <h3 class="address_title">/Адрес</h3>
                  <p class="address_sub_title">г. Санкт-Петербург<br>ул. Латышских Стрелков, д. 27, литера А, пом. 5-Н</p>
                </div>

                <div class="working-hours">
                    <h3 class="wh_title">/Режим работы</h3>
                    <p class="wh_sub_title">Пн. – Чт.: с 9:00 до 18:00<br>Пт.: с 9:00 до 17:00</p>
                  </div>

              </div>

                <div class="connect-phone-email">
                    <p class="phone">+7 812 309-86-00</p>
                    <p class="email">E-MAIL: INFO@PHC.SU></p>
                </div>
          </div>

      </div>

      <div class="form-content_block" v-if="!tabs"> 

        <div class="first_block">
            <p class="dscr">
              Заполните форму и наш менеджер<br> свяжется с вами и ответит на ваши вопросы
            </p>
        </div>

        <div class="second_block">
          <div class="placeholders">
            <input class="input" type="text" placeholder="Компания*">
            <input class="input" type="text" placeholder="Телефон*">
            <input class="input" type="text" placeholder="ФИО*">
            <input class="input" type="text" placeholder="Электронная почта*">
            <input class="input" type="text" placeholder="Запрос*">
          </div>

          <span class="file">            
            Прикрепить файл
            <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20" fill="none">
              <path d="M14.0009 0C17.3146 0 20.0009 2.68629 20.0009 6C20.0009 7.5373 19.4188 8.9843 18.397 10.0835L18.2071 10.2784L9.48 19.0053L9.4269 19.0548L9.3711 19.0997C8.7019 19.6759 7.84692 20 6.94388 20C4.88877 20 3.22277 18.334 3.22277 16.2789C3.22277 15.3775 3.54579 14.5248 4.11833 13.8574L4.26662 13.6945L4.2817 13.6826L11.5727 6.37879C11.9629 5.98793 12.5961 5.98737 12.9869 6.37755C13.3778 6.76774 13.3783 7.4009 12.9882 7.79177L5.69715 15.0956L5.68622 15.1039C5.38992 15.4208 5.22277 15.8354 5.22277 16.2789C5.22277 17.2294 5.99333 18 6.94388 18C7.32283 18 7.68077 17.8781 7.9751 17.6571L8.0972 17.5564L8.098 17.558L16.8004 8.8571L16.959 8.6927C17.6241 7.96299 18.0009 7.0125 18.0009 6C18.0009 3.79086 16.21 2 14.0009 2C12.9393 2 11.9463 2.4146 11.2058 3.13858L11.051 3.29842L11.0326 3.31139L1.70726 12.6403C1.31683 13.0309 0.683659 13.031 0.293049 12.6406C-0.0975613 12.2501 -0.0977012 11.617 0.292739 11.2264L9.6017 1.91324L9.6483 1.87021C10.7722 0.68577 12.3326 0 14.0009 0Z" fill="#3064C7"/>
            </svg>
          </span>

          
          <div class="politcal"> 
            <UiButtonCheckBox></UiButtonCheckBox>

            <p class="political-documentation">
               Я согласен с
              <span class="text">Политикой конфиденциальности</span>
            </p>
          </div>

          <UiButtonSendButton></UiButtonSendButton>
          
        </div>

      </div>

    </div>




  </section>
</template>


<style lang="scss" scoped> 

.file{
  color: #3064C7;
  font-family: "Myriad Pro";
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%; 
}

.political-documentation{
  color: #808080;
  font-family: "Myriad Pro";
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%; 
  & .text{
    color: #000;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    border-bottom: 1px solid #000;
  }
}

.placeholders{
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  grid-gap: 20px;
  margin-bottom: 20px;
}

.input{
  width: 100%;
  height: 100%;
  display: flex;
  padding: 10px 0px;
  outline: none;
  border: none;
  border-bottom: 1px solid #D9D9D9;
  &:nth-child(5){
    grid-column: 1 / -1;
  }
}

.politcal{
  margin: 30px 0px;
  display: flex;
  gap: 10px;
}

.form-content_block{
  display: flex;
  padding: 30px
}

.connect-phone-email{
  margin-top: 120px;
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.email{
  color: #000;
  font-family: "Century Gothic";
  font-size: 70px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%; 
  letter-spacing: -1.4px;
  text-transform: uppercase;
}

.phone{
  color: #000;
  font-family: "Century Gothic";
  font-size: 70px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%; 
  letter-spacing: -1.4px;
  text-transform: uppercase;
}

.connect-details{
  display: flex;
  gap: 194px;
}

.working-hours{
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.address{
  display: flex;
  gap: 20px;
  flex-direction: column;
}

.wh_sub_title{
  color: #000;
  font-family: "Myriad Pro";
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%;
}

.wh_title{
  color:  #808080;
  font-family: "Myriad Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%;
}

.address_sub_title{
  color: #000;
  font-family: "Myriad Pro";
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%;
  width: 271px;
}

.address_title{
  color:  #808080;
  font-family: "Myriad Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%;
}

.dscr{
  color: #000;
  font-family: "Myriad Pro";
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%;
}

.contact-content_block{
  display: flex;
  padding: 30px
}


.first_block{
  display: flex;
  flex-basis: 50%;
}

.second_block{
  display: flex;
  flex-direction: column;
  flex-basis: 50%;
}

.contact-block_top{
  display: flex;
}

.connect{
 flex-basis: 50%;
 width: 100%;
}

.form{
  flex-basis: 50%;
  width: 100%;
  }

.contact-button{
  color: #D9D9D9;
  background-color: #F7F7F7;
  font-family: "Myriad Pro";
  font-size: 38px;
  font-style: normal;
  font-weight: 600;
  line-height: 100%; 
  text-transform: uppercase;
  display: flex;
  align-items: center;
  width: 100%;
  padding: 30px;
  gap: 10px;
  cursor: pointer;
}

.active {
  background: #fff !important;
  color: #17172D !important;
}

.contact-button:hover{
  background: #f7f7f7bd;
}
</style>