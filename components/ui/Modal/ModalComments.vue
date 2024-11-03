<template>
  <div class="modal__comments">
    <div class="modal__comments-header">
      <h2>Оставьте комментарий к вашему товару</h2>
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="13"
        height="13"
        viewBox="0 0 13 13"
        fill="none"
        @click="$emit('closeModal')"
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
    </div>
    <input type="text" class="modal__comments-input" />
    <button class="modal__comments-button">Сохранить</button>
  </div>
</template>

<style lang="scss" scoped>
.modal__comments {
  background: #17172d;
  padding: 20px;
  &-input {
    background: var(--, #fff);
  }

  &-header {
    display: flex;
    justify-content: space-between;

    & h2 {
      color: #fff;
      font-family: "Myriad Pro";
      font-size: 20px;
      font-style: normal;
      font-weight: 600;
      line-height: 100%;
      text-transform: uppercase;
      max-width: 240px;
    }
  }
}
</style>
