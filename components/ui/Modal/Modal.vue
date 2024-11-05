<template>
  <section class="modal">
    <div class="overlay"></div>
    <div class="modal__popup">
      <div class="modal__popup-container">
        <div class="modal__popup-box">
          <button
            class="modal__popup-button--closer"
            @click="$emit('closeModal')"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="25"
              height="25"
              viewBox="0 0 25 25"
              fill="none"
            >
              <path
                d="M0.237178 0.489985L0.354307 0.354307C0.783775 -0.075161 1.45581 -0.114193 1.92937 0.237178L2.06505 0.354307L12.5 10.7887L22.935 0.354307C23.4074 -0.118096 24.1732 -0.118096 24.6457 0.354307C25.1181 0.826711 25.1181 1.59265 24.6457 2.06505L14.2113 12.5L24.6457 22.935C25.0752 23.3644 25.1142 24.0365 24.7628 24.51L24.6457 24.6457C24.2163 25.0752 23.5442 25.1142 23.0707 24.7628L22.935 24.6457L12.5 14.2113L2.06505 24.6457C1.59265 25.1181 0.826711 25.1181 0.354307 24.6457C-0.118096 24.1732 -0.118096 23.4074 0.354307 22.935L10.7887 12.5L0.354307 2.06505C-0.075161 1.63558 -0.114193 0.96355 0.237178 0.489985Z"
                fill="#212121"
              />
            </svg>
          </button>

          <div class="modal__popup-inputs">
            <input
              type="text"
              class="modal__popup-input"
              placeholder="Название реквизита*"
            />
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
            <input type="text" class="modal__popup-input" placeholder="ИНН*" />
            <input type="text" class="modal__popup-input" placeholder="КПП*" />
            <input type="text" class="modal__popup-input" placeholder="ОГРН*" />
            <input type="text" class="modal__popup-input" placeholder="ОКПО*" />
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
            <input type="text" class="modal__popup-input" placeholder="БИК*" />
            <input
              type="text"
              class="modal__popup-input"
              placeholder="Телефон*"
            />
          </div>
          <UiButtonSendButton>Сохранить</UiButtonSendButton>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
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
  &__popup-button--closer {
    position: absolute;
    top: 30px;
    left: 995px;
    background-color: white;
    cursor: pointer;
  }
  &__popup {
    position: absolute;
    z-index: 100;
    top: 100px;
    left: 435px;
    width: 1050px;
    padding: 60px;
    background: white;
  }

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
    &:nth-child(1) {
      grid-column: 1 / -1;
    }
  }
}
</style>
