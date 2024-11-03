<script setup lang="ts">
const route = useRoute();

const tabs = ref(true);
</script>

<template>
  <section class="contacts container">
    <h2 class="contacts__title">Контакты</h2>

    <div class="contacts__content">
      <div class="contacts__header">
        <button
          :class="`contacts__tab-button ${tabs ? 'contacts__tab-button--active' : ''}`"
          @click="tabs = true"
        >
          <svg width="10" height="10" viewBox="0 0 10 10" fill="none" xmlns="http://www.w3.org/2000/svg">
            <rect width="10" height="10" fill="currentColor" />
          </svg>
          Свяжитесь с нами
        </button>

        <button
          :class="`contacts__tab-button ${!tabs ? 'contacts__tab-button--active' : ''}`"
          @click="tabs = false"
        >
          <svg width="10" height="10" viewBox="0 0 10 10" fill="none" xmlns="http://www.w3.org/2000/svg">
            <rect width="10" height="10" fill="currentColor" />
          </svg>
          Форма заявки
        </button>
      </div>
    </div>

    <div class="contacts__connect-mob">
        <span class="contacts__connect-title--mob">
          <svg width="10" height="10" viewBox="0 0 10 10" fill="none" xmlns="http://www.w3.org/2000/svg">
            <rect width="10" height="10" fill="currentColor" />
          </svg>
          Свяжитесь с нами
        </span>

        <span class="contacts__connect-subtitle--mob">
          Свяжитесь с нами и мы ответим на вопросы
        </span>

        <div class="contacts__column--second">
          <div class="contacts__details">
            
            <div class="contacts__address">
              <h3 class="contacts__address-title">/Адрес</h3>
              <p class="contacts__address-text">
                г. Санкт-Петербург<br />ул. Латышских Стрелков, д. 27, литера А, пом. 5-Н
              </p>
            </div>

            <div class="contacts__hours">
              <h3 class="contacts__hours-title">/Режим работы</h3>
              <p class="contacts__hours-text">
                Пн. – Чт.: с 9:00 до 18:00<br />Пт.: с 9:00 до 17:00
              </p>
            </div>
          </div>

          <div class="contacts__contact-info">
            <p class="contacts__phone">+7 812 309-86-00</p>
            <p class="contacts__email">E-MAIL: INFO@PHC.SU</p>
          </div>
        </div>
     </div>

    <div class="contacts__form-mob">
      <div class="contacts__info">
        <span class="contacts__form-title">
          <svg width="10" height="10" viewBox="0 0 10 10" fill="none" xmlns="http://www.w3.org/2000/svg">
            <rect width="10" height="10" fill="currentColor" />
          </svg>
          Форма заявки
        </span>

          <p class="contacts__description">
            Заполните форму и наш менеджер свяжется с вами и ответит на ваши вопросы
          </p>
        </div>
        <div class="contacts__form">
          <div class="contacts__form-inputs">
          <input class="contacts__input" type="text" placeholder="Компания*" />
          <input class="contacts__input" type="text" placeholder="Телефон*" />
          <input class="contacts__input" type="text" placeholder="ФИО*" />
          <input class="contacts__input" type="text" placeholder="Электронная почта*" />
          <input class="contacts__input" type="text" placeholder="Запрос*" />
          </div>

            <span class="contacts__file-upload">
              Прикрепить файл
              <svg xmlns="http://www.w3.org/2000/svg" width="15" height="16" viewBox="0 0 15 16" fill="#3064C7">
                <path d="M10.5002 0.5C12.9854 0.5 15 2.51472 15 5C15 6.15298 14.5634 7.23822 13.7971 8.06262L13.6547 8.2088L7.10968 14.754L7.06986 14.7911L7.02801 14.8248C6.52613 15.2569 5.88492 15.5 5.20767 15.5C3.66641 15.5 2.41697 14.2505 2.41697 12.7092C2.41697 12.0331 2.65922 11.3936 3.08861 10.8931L3.19982 10.7709L3.21113 10.7619L8.67913 5.28409C8.97177 4.99095 9.44665 4.99053 9.73974 5.28316C10.0329 5.57581 10.0333 6.05067 9.74071 6.34383L4.27267 11.8217L4.26447 11.8279C4.04226 12.0656 3.9169 12.3765 3.9169 12.7092C3.9169 13.4221 4.49479 14 5.20767 14C5.49187 14 5.76032 13.9086 5.98106 13.7428L6.07263 13.6673L6.07323 13.6685L12.5997 7.14282L12.7187 7.01953C13.2175 6.47224 13.5001 5.75938 13.5001 5C13.5001 3.34314 12.157 2 10.5002 2C9.70404 2 8.95932 2.31095 8.40397 2.85393L8.28788 2.97381L8.27408 2.98354L1.28039 9.98022C0.987577 10.2732 0.512721 10.2733 0.219777 9.98045C-0.0731677 9.68758 -0.0732726 9.21275 0.219544 8.9198L7.20095 1.93493L7.2359 1.90266C8.07879 1.01433 9.24903 0.5 10.5002 0.5Z" fill="#3064C7"/>
              </svg>
            </span>

            <div class="contacts__consent">
              <UiButtonCheckBox></UiButtonCheckBox>
              <p class="contacts__privacy">
                Я согласен с <a class="contacts__privacy-link" href="">Политикой конфиденциальности</a>
              </p>
            </div>

            <UiButtonSendButton></UiButtonSendButton>
        </div>
    </div>

     <div class="contacts__connect-content" v-if="tabs">
        <div class="contacts__column contacts__column--first">
          <p class="contacts__description">
            Свяжитесь с нами и мы ответим на вопросы
          </p>
        </div>
        
        <div class="contacts__column contacts__column--second">
          <div class="contacts__details">
            
            <div class="contacts__address">
              <h3 class="contacts__address-title">/Адрес</h3>
              <p class="contacts__address-text">
                г. Санкт-Петербург<br />ул. Латышских Стрелков, д. 27, литера А, пом. 5-Н
              </p>
            </div>

            <div class="contacts__hours">
              <h3 class="contacts__hours-title">/Режим работы</h3>
              <p class="contacts__hours-text">
                Пн. – Чт.: с 9:00 до 18:00<br />Пт.: с 9:00 до 17:00
              </p>
            </div>
          </div>

          <div class="contacts__contact-info">
            <p class="contacts__phone">+7 812 309-86-00</p>
            <p class="contacts__email">E-MAIL: INFO@PHC.SU</p>
          </div>
        </div>
      </div>

      <div class="contacts__form-content" v-if="!tabs">
        <div class="contacts__info">
          <p class="contacts__description">
            Заполните форму и наш менеджер свяжется с вами и ответит на ваши вопросы
          </p>
        </div>
        <div class="contacts__form">
          <div class="contacts__form-inputs">
          <input class="contacts__input" type="text" placeholder="Компания*" />
          <input class="contacts__input" type="text" placeholder="Телефон*" />
          <input class="contacts__input" type="text" placeholder="ФИО*" />
          <input class="contacts__input" type="text" placeholder="Электронная почта*" />
          <input class="contacts__input" type="text" placeholder="Запрос*" />
          </div>

            <span class="contacts__file-upload">
              Прикрепить файл
              <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20" fill="none">
                <path d="M14.0009 0C17.3146 0 20.0009 2.68629 20.0009 6C20.0009 7.5373 19.4188 8.9843 18.397 10.0835L18.2071 10.2784L9.48 19.0053L9.4269 19.0548L9.3711 19.0997C8.7019 19.6759 7.84692 20 6.94388 20C4.88877 20 3.22277 18.334 3.22277 16.2789C3.22277 15.3775 3.54579 14.5248 4.11833 13.8574L4.26662 13.6945L4.2817 13.6826L11.5727 6.37879C11.9629 5.98793 12.5961 5.98737 12.9869 6.37755C13.3778 6.76774 13.3783 7.4009 12.9882 7.79177L5.69715 15.0956L5.68622 15.1039C5.38992 15.4208 5.22277 15.8354 5.22277 16.2789C5.22277 17.2294 5.99333 18 6.94388 18C7.32283 18 7.68077 17.8781 7.9751 17.6571L8.0972 17.5564L8.098 17.558L16.8004 8.8571L16.959 8.6927C17.6241 7.96299 18.0009 7.0125 18.0009 6C18.0009 3.79086 16.21 2 14.0009 2C12.9393 2 11.9463 2.4146 11.2058 3.13858L11.051 3.29842L11.0326 3.31139L1.70726 12.6403C1.31683 13.0309 0.683659 13.031 0.293049 12.6406C-0.0975613 12.2501 -0.0977012 11.617 0.292739 11.2264L9.6017 1.91324L9.6483 1.87021C10.7722 0.68577 12.3326 0 14.0009 0Z" fill="#3064C7"/>
              </svg>
            </span>

            <div class="contacts__consent">
              <UiButtonCheckBox></UiButtonCheckBox>
              <p class="contacts__privacy">
                Я согласен с <a class="contacts__privacy-link" href="">Политикой конфиденциальности</a>
              </p>
            </div>

            <UiButtonSendButton></UiButtonSendButton>
        </div>
      </div>

  </section>
</template>


<style lang="scss" scoped>
.contacts {
  &__form-mob{
    display: none;
  }

  &__connect-mob {
    display: none;
  }

  &__info{
    flex-basis: 50%
  }
  

  &__title {
    padding: 30px 0;
    color: #000;
    font-family: "Century Gothic";
    font-size: 105px;
    font-weight: 700;
    line-height: 90%;
    text-transform: uppercase;
  }

  &__file-upload {
    display: flex;
    align-items: center;
    gap: 5px;
    color: #3064c7;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-weight: 400;
    line-height: 100%;
  }

  &__privacy {
    color: #808080;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-weight: 400;
    line-height: 100%;

    &-link {
      color: #000;
      text-decoration: underline;
    }
  }

  &__input {
      color: #808080;
      font-family: "Myriad Pro";
      font-size: 24px;
      font-weight: 400;
      line-height: 100%;
      padding: 10px 0;
      outline: none;
      border: none;
      border-bottom: 1px solid #d9d9d9;

      &:nth-child(5) {
        grid-column: 1 / -1;
      }
    }

  &__form {
    flex-basis: 50%;
    &-inputs{
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    grid-gap: 20px;
    margin-bottom: 20px;
    }
  }

  &__consent {
    margin: 30px 0;
    display: flex;
    gap: 10px;
  }

  &__form-content {
    display: flex;
    padding: 30px;
  }

  &__contact-info {
    margin-top: 120px;
    display: flex;
    flex-direction: column;
    gap: 15px;
  }

  &__email, &__phone {
    color: #000;
    font-family: "Century Gothic";
    font-size: 70px;
    font-weight: 700;
    line-height: 90%;
    letter-spacing: -1.4px;
    text-transform: uppercase;
  }

  &__details {
    display: flex;
    gap: 194px;
  }

  &__hours, &__address {
    display: flex;
    flex-direction: column;
    gap: 20px;

    &-text {
      color: #000;
      font-family: "Myriad Pro";
      font-size: 24px;
      font-weight: 400;
      line-height: 100%;
    }

    &-title {
      color: #808080;
      font-family: "Myriad Pro";
      font-size: 20px;
      font-weight: 400;
      line-height: 100%;
    }
  }

  &__description {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-weight: 400;
    line-height: 100%;
    max-width: 460px;
  }

  &__connect-content {
    display: flex;
    padding: 30px;
  }

  &__column {
    &--first {
      flex-basis: 50%;
    }

    &--second {
      display: flex;
      flex-direction: column;
      flex-basis: 50%;
    }
  }

  &__header {
    display: flex;
  }

  &__tab {
    &--connect, &--form {
      flex-basis: 50%;
      width: 100%;
    }

    &-button {
      color: #d9d9d9;
      background-color: #f7f7f7;
      font-family: "Myriad Pro";
      font-size: 38px;
      font-weight: 600;
      line-height: 100%;
      text-transform: uppercase;
      display: flex;
      align-items: center;
      width: 100%;
      padding: 30px;
      gap: 10px;
      cursor: pointer;

      &--active {
        background: #fff !important;
        color: #17172d !important;
      }

      &:hover {
        background: #f7f7f7bd;
      }
    }
  }
}


@media screen and (max-width: 1439.99px) {
}

@media screen and (max-width: 1199.99px) {
  .contacts{
    &__connect-content{
      flex-direction: column;
      gap: 20px;
    }
    &__form-content{
      flex-direction: column;
      gap: 20px;
    }
    &__description{
      max-width: 100%;
    }
    &__details{
      gap: 140px;
    }
  }
}

@media screen and (max-width: 991.99px) {
  .contacts{
    &__description{
      font-size: 22px;
    }
    &__tab-button{
      font-size: 30px;
    }
    &__phone, &__email{
        font-size: 60px;
    }
    &__address-text, &__hours-text{
      font-size: 18px;
    }
    &__details{
      gap: 100px;
    }
    &__title{
      font-size: 80px;
    }
  }
}

@media screen and (max-width: 767.99px) {
  .contacts{
    &__phone, &__email{
        font-size: 40px;
    }
    &__details{
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    &__contact-info{
      margin-top: 20px;
    }
    &__tab-button{
      font-size: 20px;
    }
    &__description{
      font-size: 18px;
    }
    &__input{
      font-size: 20px;
    }
    &__file-upload{
      font-size: 20px;
    }
    &__privacy{
      font-size: 20px;
    }
    &__title{
      font-size: 50px;
    }
  }
}

@media screen and (max-width: 539.99px) {
  .contacts{
    &__tab-button{
      font-size: 14px;
    }
    &__form-content{
      flex-direction: column;
    }
    &__form-inputs{
      grid-template-columns: repeat(1, minmax(0, 1fr));
    }
    &__description{
      font-size: 15px
    }
    &__input{
      font-size: 18px;
    }
    &__file-upload{
      font-size: 18px;
    }
    &__privacy{
      font-size: 15px;
    }
  }
}

@media screen and (max-width: 424.99px) {
  .contacts{
    &__tab-button{
      font-size: 12px;
    }
    &__privacy{
      font-size: 12px;
      display: flex;
      align-items: center;
      gap: 5px;
    }
    &__phone , &__email{
      font-size: 30px;
    }
  }
}

@media screen and (max-width: 375.99px) {
  .contacts{
    &__connect-content{
      display: none;
    }
    &__form-content{
      display: none;
    }
    &__content{
      display: none;
    }
    &__title{
      font-size: 50px;
    }
    &__connect-mob{
      display: block;
      display: flex;
      flex-direction: column;
      gap: 20px;
      margin-bottom: 60px;
      & svg{
        width: 5px;
        height: 5px;
      }
    }

    &__connect-subtitle--mob{
      color: #000;
      font-family: "Myriad Pro";
      font-size: 17px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
      }

    &__connect-title--mob{
        display: flex;
        align-items: center;
        gap: 5px;
        color: #000;
        font-family: "Myriad Pro";
        font-size: 24px;
        font-style: normal;
        font-weight: 600;
        line-height: 100%; 
        text-transform: uppercase;
      }
    &__column--second{
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    &__details{
      flex-direction: column;
      gap: 20px;
    }
    &__address{
      gap: 10px;
    }
    &__contact-info{
      margin: unset;
    }
    &__email , &__phone{
      color: #17172D;
      font-family: "Myriad Pro";
      font-size: 20px;
      font-style: normal;
      font-weight: 600;
      line-height: 90%; 
      }

      &__form-mob{
        display: flex;
        flex-direction: column;
        gap: 20px;
        margin-bottom: 60px;
        & svg{
          width: 5px;
          height: 5px;
        }
      }
      &__form-title{
        display: flex;
        align-items: center;
        gap: 5px;
        color: #000;
        font-family: "Myriad Pro";
        font-size: 24px;
        font-style: normal;
        font-weight: 600;
        line-height: 100%;
        text-transform: uppercase;
      }
      &__info{
        display: flex;
        flex-direction: column;
        gap: 20px;
      }
      &__description{
        color: #000;
        font-family: "Myriad Pro";
        font-size: 17px;
        font-style: normal;
        font-weight: 400;
        line-height: 100%;
      }
      &__form-inputs{
        gap: 15px;
        grid-template-columns: repeat(1, minmax(0, 1fr));
        margin-bottom: 15px;
      }
      &__file-upload {
        & svg{
          width: 16px;
          height: 16px;
        }
      }
      &__privacy{
        color:#808080;
        font-family: "Myriad Pro";
        font-size: 15px;
        font-style: normal;
        font-weight: 400;
        line-height: 100%; 
      }
      &__privacy-link{
        color: #3064C7;
        font-family: "Myriad Pro";
        font-size: 15px;
        font-style: normal;
        font-weight: 400;
        line-height: 100%;
        text-decoration-line: underline;
      }
      &__consent{
        margin: 18.5px 0px;
        display: flex;
        align-items: center;
      }
      &__input{
        color: #808080;
        font-family: "Myriad Pro";
        font-size: 18px;
        font-style: normal;
        font-weight: 400;
        line-height: 100%; 
      }
      &__file-upload{
      display: flex;
      gap: 5px;
      align-items: center;
      color: #3064C7;
      font-family: "Myriad Pro";
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
      }
  }

}
</style>
