<script setup>
const list = ref([
  { id: 1, name: "asdasd", quantity: 1, cost: 500 },
  { id: 2, name: "asdasd", quantity: 1, cost: 500 },
  { id: 3, name: "asdasd", quantity: 1, cost: 500 },
]);

const isOpen = ref(false);

const closeModal = () => {
  isOpen.value = false;
};
</script>

<template>
  <UiModalComments
    v-if="isOpen"
    @closeModal="closeModal"
    @click.stop
    class="typeproduct__content-table-modal-acc"
  ></UiModalComments>
  <table class="typeproduct__content-table">
    <thead class="typeproduct__content-table-thead">
      <tr class="typeproduct__content-table-table-row">
        <th class="typeproduct__content-table-th">Артикул</th>
        <th class="typeproduct__content-table-th">PN</th>
        <th class="typeproduct__content-table-th">DN</th>
        <th class="typeproduct__content-table-th">Материал</th>
        <th class="typeproduct__content-table-th">Резьба</th>
        <th class="typeproduct__content-table-th">Размер L</th>
        <th class="typeproduct__content-table-th">В наличии</th>
        <th class="typeproduct__content-table-th">Цена</th>
        <th class="typeproduct__content-table-th">Комментарий</th>
        <th class="typeproduct__content-table-th">Количество</th>
        <th class="typeproduct__content-table-th">Купить</th>
      </tr>
    </thead>
    <tbody class="typeproduct__content-table-tbody">
      <tr
        v-for="item in list"
        :key="item.id"
        class="typeproduct__content-table-table-row"
      >
        <td class="typeproduct__content-table-td">{{ item.name }}</td>
        <td class="typeproduct__content-table-td">500</td>
        <td class="typeproduct__content-table-td">6</td>
        <td class="typeproduct__content-table-td">Нержавеющая сталь</td>
        <td class="typeproduct__content-table-td">M16*1.5</td>
        <td class="typeproduct__content-table-td">69</td>
        <td class="typeproduct__content-table-td">100</td>
        <td class="typeproduct__content-table-td">{{ item.cost }}</td>
        <td class="typeproduct__content-table-td">
          <div class="typeproduct__content-table-modal">
            <button
              class="typeproduct__content-table-modal-svg"
              @click="isOpen = !isOpen"
            >
              <UiIconComents :isActive="true"></UiIconComents>
            </button>
          </div>
        </td>
        <td class="typeproduct__content-table-td">
          <div class="counter">
            <UiCounter></UiCounter>
          </div>
        </td>
        <td class="typeproduct__content-table-td">
          <div class="typeproduct__content-table-buttons">
            <button class="typeproduct__content-table-button">В корзину</button>
            <button class="typeproduct__content-table-favorite">
              <UiIconFavorites></UiIconFavorites>
            </button>
          </div>
        </td>
      </tr>
    </tbody>
  </table>
</template>

<style lang="scss" scoped>
.counter {
  display: flex;
  width: 100%;
  justify-content: center;
}
.typeproduct {
  margin-top: 20px;
  &__banner {
    background: #f6f6f6;
    padding: 30px;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 20px;
    & h1 {
      color: #000;
      font-family: "Century Gothic";
      font-size: 100px;
      font-style: normal;
      font-weight: 700;
      line-height: 90%;
      text-transform: uppercase;
      text-align: center;
      max-width: 1280px;
      & span {
        color: #3064c7;
        text-align: center;
        font-family: "Century Gothic";
        font-size: 100px;
        font-style: normal;
        font-weight: 700;
        line-height: 90%; /* 90px */
        text-transform: uppercase;
      }
    }
    & img {
      max-width: 354px;
      margin: -15px;
    }
  }
  &__content {
    margin-bottom: 130px;

    &-table {
      & {
        border-collapse: collapse;
        width: 100%;
      }
      &-modal {
        position: relative;
        &-svg {
          cursor: pointer;
          background: transparent;
        }
      }
      &-buttons {
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 10px;
      }
      &-button {
        color: #fff;
        border-radius: 3px;
        background: #3064c7;
        font-family: "Myriad Pro";
        font-size: 20px;
        font-style: normal;
        font-weight: 600;
        line-height: 90%;
        text-transform: uppercase;
        padding: 10px 25px;
        cursor: pointer;
        transition: 0.3s;
        &:hover {
          background: #10316d;
        }
      }
      &-favorite {
        background: transparent;
        cursor: pointer;
      }

      & {
        border: 1px solid #d9d9d9;
      }
      &-td {
        padding: 20px 0;
        color: #000;
        text-align: center;
        font-family: "Myriad Pro";
        font-size: 18px;
        font-style: normal;
        font-weight: 400;
        line-height: 90%;
        text-align: center;
        border: 1px solid #d9d9d9;
      }
      &-th {
        color: #000;
        text-align: center;
        font-family: "Myriad Pro";
        font-size: 20px;
        font-style: normal;
        font-weight: 600;
        line-height: 90%;
        text-transform: uppercase;
        border: 1px solid #d9d9d9;
        padding: 20px 0;
      }
    }
  }
  &__filter {
    margin-top: 30px;
    background: #17172d;
    margin-bottom: 10px;
    padding: 20px;
    width: 100%;
    &-title {
      color: #fff;
      font-family: "Myriad Pro";
      font-size: 38px;
      font-style: normal;
      font-weight: 600;
      line-height: 100%;
      text-transform: uppercase;
    }
    &s {
      display: flex;
      flex-grow: 1;
      gap: 30px;
      width: 100%;
    }
  }
}
</style>
