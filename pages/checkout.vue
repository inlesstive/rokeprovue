<template>
  <div class="checkout container">
    <h1>Оформление заказа</h1>
    <div class="checkout__content">
      <div class="checkout__content-side">
        <div class="checkout__content-side-delivery">
          <h3 class="checkout__content-side-delivery-title">Доставка</h3>
          <div class="checkout__content-side-delivery-flex">
            <button class="checkout__content-side-delivery-button active">
              Самовывоз
            </button>
            <button class="checkout__content-side-delivery-button">
              Транспортная компания
            </button>
          </div>
        </div>
        <div class="checkout__content-side-details">
          <div class="checkout__content-side-details-title">
            <h3>Оплата</h3>
            <select
              class="checkout__content-side-details-title-select"
              name=""
              id=""
            >
              <option value="" selected>Выбрать существующие</option>
              <option value="">Roke</option>
              <option value="">Roke</option>
              <option value="">Roke</option>
              <option value="">Roke</option>
            </select>
          </div>
          <div class="modal__popup-box">
            <div class="modal__popup-inputs">
              <input
                type="text"
                class="modal__popup-input"
                placeholder="Полное фирменное наименование**"
              />
              <input
                type="text"
                class="modal__popup-input"
                placeholder="Электронная почта*"
              />
              <input
                type="text"
                class="modal__popup-input"
                placeholder="ИНН*"
              />
              <input
                type="text"
                class="modal__popup-input"
                placeholder="КПП*"
              />
              <input
                type="text"
                class="modal__popup-input"
                placeholder="ОГРН*"
              />
              <input
                type="text"
                class="modal__popup-input"
                placeholder="ОКПО*"
              />
              <input
                type="text"
                class="modal__popup-input"
                placeholder="ОКАТО*"
              />
              <input
                type="text"
                class="modal__popup-input"
                placeholder="ОКТМО*"
              />
              <input
                type="text"
                class="modal__popup-input"
                placeholder="Юридический адрес*"
              />
              <input
                type="text"
                class="modal__popup-input"
                placeholder="Почтовый адрес*"
              />
              <input
                type="text"
                class="modal__popup-input"
                placeholder="БИК*"
              />
              <input
                type="text"
                class="modal__popup-input"
                placeholder="Телефон*"
              />
            </div>
            <button class="modal__popup-button">Сохранить</button>
          </div>
        </div>
      </div>
      <div class="checkout__content-side side-2">
        <div class="checkout__content-side-next-step">
          <div class="checkout__content-side-next-step-price">
            <span>Итого</span>
            <span>1 000 ₽</span>
          </div>
          <div class="checkout__content-side-next-step-sallary">
            <span>Товаров на сумму</span>
            <span>1 000 ₽</span>
          </div>
          <UiButtonSendButton>Перейти к оформлению</UiButtonSendButton>
          <div class="checkout__content-side-next-step-privacy">
            Согласен с условиями
            <NuxtLink to="/">Пользовательского соглашения</NuxtLink> и
            <NuxtLink to="/">Политики конфиденциальности</NuxtLink>
          </div>
        </div>

        <div class="checkout__content-side-table">
          <h2>У вас в заказе</h2>
          <table>
            <thead>
              <tr>
                <th>Товар</th>
                <th>Количество</th>
                <th>Итого</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="_ in 10">
                <td>
                  Шаровый гидравлический кран высокого давления с двойной
                  резьбой PN 500 DN 6
                </td>
                <td>
                  <UiCounter></UiCounter>
                </td>
                <td>500 000 ₽</td>
              </tr>
            </tbody>
          </table>
          <UiTableMobile></UiTableMobile>
        </div>
      </div>
    </div>
  </div>
</template>
<script setup></script>

<style lang="scss" scoped>
h1 {
  color: #000;

  font-family: "Century Gothic";
  font-size: 105px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%;
  text-transform: uppercase;
}
table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 20px;
  & th {
    padding: 17px;
    color: #000;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%; /* 18px */
  }
  & td {
    padding: 20px;
    color: #000;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%; /* 24px */
    max-width: 550px;
  }
  & th,
  td {
    border: 1px solid #d9d9d9;
  }
}
.checkout {
  margin-top: 20px;
  margin-bottom: 20px;

  &__content {
    display: flex;
    gap: 20px;

    &-side {
      flex-basis: 50%;
      margin-top: 60px;
      &-details {
        margin-top: 60px;
        margin-bottom: 30px;
        &-title {
          display: flex;
          justify-content: space-between;
          color: #000;
          font-family: "Myriad Pro";
          font-size: 40px;
          font-style: normal;
          font-weight: 400;
          line-height: 90%; /* 36px */
          &-select {
            background-color: #fff;
            border: 1px solid #d9d9d9;
            background: #fff;
            outline: none;
            padding: 10px;
          }
        }
      }
      &-delivery {
        &-title {
          color: #000;
          font-family: "Myriad Pro";
          font-size: 40px;
          font-style: normal;
          font-weight: 400;
          line-height: 90%;
        }
        &-button {
          color: #3064c7;
          background: transparent;
          padding: 10px;
          color: #000;
          font-family: "Myriad Pro";
          font-size: 20px;
          font-style: normal;
          font-weight: 400;
          line-height: 100%;
          border: 1px solid #d9d9d9;
          cursor: pointer;
          &.active {
            color: #3064c7;
            border: 1px solid #3064c7;
          }
        }
        &-flex {
          display: flex;
          gap: 10px;
          margin-top: 20px;
        }
      }
      & h2 {
        margin-top: 20px;
        color: #000;
        font-family: "Myriad Pro";
        font-size: 30px;
        font-style: normal;
        font-weight: 400;
        line-height: 90%;
      }
      &-next-step {
        padding: 20px;
        border: 1px solid #d9d9d9;
        &-price {
          display: flex;
          justify-content: space-between;
          & span {
            color: #000;
            font-family: "Myriad Pro";
            font-size: 38px;
            font-style: normal;
            font-weight: 600;
            line-height: 100%; /* 38px */
          }
        }
        &-privacy {
          color: #17172d;
          font-family: "Myriad Pro";
          font-size: 18px;
          font-style: normal;
          font-weight: 400;
          margin-top: 20px;
          line-height: 90%; /* 16.2px */
          & a {
            color: #3064c7;
            font-family: "Myriad Pro";
            font-size: 18px;
            font-style: normal;
            font-weight: 400;
            line-height: 90%;
          }
        }
        &-sallary {
          display: flex;
          justify-content: space-between;
          margin-top: 10px;
          margin-bottom: 20px;
          & span {
            color: #000;

            /* Текст 5 */
            font-family: "Myriad Pro";
            font-size: 24px;
            font-style: normal;
            font-weight: 400;
            line-height: 100%; /* 24px */
          }
        }
      }
    }
  }
}

.overlay {
  position: fixed;
  width: 100vw;
  height: 100vh;
  top: 0;
  left: 0;
  background: black;
  opacity: 0.6;
}

.modal {
  &__popup-container {
    display: flex;
    flex-direction: column;
  }
  &__popup-inputs {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    grid-gap: 30px;
    margin-bottom: 30px;
  }
  &__popup-button {
    color: #000;

    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 600;
    line-height: 90%;
    text-transform: uppercase;
    background: transparent;
    width: 100%;
    border: 1px solid #d9d9d9;
    padding: 20px;
    cursor: pointer;
  }

  &__popup-input {
    color: #808080;
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
    border-bottom: 1px solid #d9d9d9;
  }
}

@media screen and (max-width: 1439.99px) {
}

@media screen and (max-width: 1199.99px) {
  .checkout__content {
    display: flex;
    gap: 20px;
    flex-direction: column;
  }
}

@media screen and (max-width: 991.99px) {
  h1 {
    font-size: 75px;
  }
  .modal__popup-input{
    font-size: 22px;
  }
}

@media screen and (max-width: 767.99px) {
  .modal__popup-input{
    font-size: 20px;
  }
  .side-2 {
    display: flex;
    flex-direction: column-reverse;
    gap: 20px;
  }
  .checkout__content-side {
    flex-basis: 50%;
    margin-top: 0px;
  }
  h1 {
    font-size: 65px;
  }
  table {
    display: none;
  }
}

@media screen and (max-width: 539.99px) {
  .checkout__content-side-details-title {
    display: flex;
    justify-content: space-between;
    color: #000;
    font-family: "Myriad Pro";
    font-size: 40px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
    flex-direction: column;
    gap: 15px;
    flex-wrap: wrap;
  }
  .checkout__content-side-delivery {
    margin-top: 20px;
  }
  .modal__popup-inputs {
    display: grid;
    grid-template-columns: repeat(1, minmax(0, 1fr));
    grid-gap: 30px;
    margin-bottom: 30px;
  }
  .checkout__content-side-delivery-flex {
    display: flex;
    gap: 10px;
    margin-top: 20px;
    flex-direction: column;
  }
}

@media screen and (max-width: 424.99px) {
  h1 {
    font-size: 39px;
  }
}

@media screen and (max-width: 375.99px) {
  .modal__popup-input{
    font-size: 18px;
  }
}

@media screen and (max-width: 319.99px) {
}
</style>
