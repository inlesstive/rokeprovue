<script setup lang="ts">
defineProps<{
  placeholder?: string;
  option: string[];
}>();

const isOpen = ref(false);
</script>

<template>
  <div class="dropdown">
    <div class="dropdown__header" @click="isOpen = !isOpen">
      <button class="dropdown__header-button">
        {{ placeholder }}
        <UiIconArrowDropdown></UiIconArrowDropdown>
      </button>
    </div>
    <div class="dropdown__content" v-if="isOpen">
      <ul class="dropdown__content-list">
        <li class="dropdown__content-list-item" v-for="_ in 50">
          <UiButtonCheckBox></UiButtonCheckBox>
          <span>М 16x1,5</span>
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.dropdown {
  background-color: #fff;
  width: 150px;
  border: 1px solid #17172d;
  padding: 10px;
  position: relative;
  z-index: 10005;
  border-collapse: collapse;

  &__content {
    border-top: 0px !important;
    border: 1px solid #17172d;
    position: absolute;
    width: 100%;
    margin-top: 10px;
    z-index: 10005;
    background-color: #fff;
    left: 0;
    padding: 10px 15px;

    &-list {
      overflow: scroll;
      overflow-x: hidden;
      max-height: 200px;
      &::-webkit-scrollbar {
        width: 8px;
      }
      &::-webkit-scrollbar-thumb {
        background-color: #d9d9d9;
        border-radius: 10px;
        width: 2px;
      }
      &-item {
        display: flex;
        align-items: center;
        gap: 10px;
        & span {
          color: #17172d;
          font-size: 16px;
          font-style: normal;
          font-weight: 400;
          line-height: 90%;
        }
      }
    }
  }
  &__header {
    &-button {
      width: 100%;
      background-color: transparent;
      display: flex;

      flex-direction: row;
      justify-content: space-between;
      align-items: center;
      color: #808080;
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 90%;
      cursor: pointer;
    }
  }
}
</style>
