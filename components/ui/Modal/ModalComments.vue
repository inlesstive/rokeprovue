<template>
  <div class="modal">
    <div class="modal__overlay" @click="$emit('closeModal')"></div>
    <div class="modal__content">
      <div class="modal__content-block">
        <div class="modal__content-head">
          <span>Оставьте комментарий к вашему товару</span>
          <button @click="$emit('closeModal')">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="13"
              height="13"
              viewBox="0 0 13 13"
              fill="none"
            >
              <path
                d="M12 1L1 12"
                stroke="white"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
              <path
                d="M1 1L12 12"
                stroke="white"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </button>
        </div>
        <div class="modal__content-body">
          <textarea> </textarea>
          <button class="modal__content-body-button">Сохранить</button>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
 .modal {
  width: 100%;
  height: 100%;
  &__overlay {
    position: fixed;
    width: 100vw;
    height: 100vh;
    top: 0;
    left: 0;
    opacity: 0.5;
    background-color: #000;
    z-index: 1000000;
  }
  &__content {
    position: fixed;
    z-index: 1000001; // Уменьшите на 1, чтобы overlay был поверх
    display: flex;
    justify-content: center;
    align-items: center;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    &-body {
      & textarea {
        width: 100%;
        height: 70px;
        margin-top: 20px;
        resize: none;
        color: #000;
        font-family: "Myriad Pro";
        font-size: 18px;
        font-style: normal;
        font-weight: 400;
        line-height: 100%;
        padding: 10px;
      }
      &-button {
        padding: 9px 0;
        color: #fff;
        font-family: "Myriad Pro";
        font-size: 18px;
        font-style: normal;
        font-weight: 600;
        line-height: 90%;
        background: #3064c7;
        width: 100%;
        text-transform: uppercase;
        margin-top: 10px;
        cursor: pointer;
      }
    }

    &-head {
      display: flex;
      justify-content: space-between;
      & button {
        background: none;
        cursor: pointer;
      }
    }

    &-block {
      max-width: 381px;
      width: 100%;
      background: #17172d;
      padding: 20px;
      & span {
        color: #fff;
        max-width: 239px;
        font-family: "Myriad Pro";
        font-size: 20px;
        font-style: normal;
        font-weight: 600;
        line-height: 100%;
        text-transform: uppercase;
        max-width: 239px;
      }
    }
  }
}
</style>
