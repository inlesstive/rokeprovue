<script setup>
const route = useRoute();
const breadcrumbsData = [
  { text: "Главная", to: "/" },
  { text: "Каталог", to: "/" },
  { text: "Запорная арматура", to: "/catalog/valves/123" },
  { text: "Высокого давления", to: "/catalog/valves/high-pressure" },
];

const selectedCategory = ref(null);
const categoryOptions = ref([
  { text: "Запорная арматура", value: "armatura" },
  { text: "Кран шаровый", value: "kran" },
  { text: "Высокого давления", value: "high-pressure" },
  // Дополнительные категории
]);

const isOpen = ref(false);

const closeModal = () => {
  isOpen.value = false;
};

const list = ref([
  {
    name: "asdasd",
    quanity: 1,
    cost: 500,
  },
  {
    name: "asdasd",
    quanity: 1,
    cost: 500,
  },
  {
    name: "asdasd",
    quanity: 1,
    cost: 500,
  },
]);
</script>

<template>
  <section class="typeproduct container">
    <UiBreadCrumbs :crumbs="breadcrumbsData"></UiBreadCrumbs>
    <div class="typeproduct__banner">
      <h1><span>Шаровые</span> гидравлические краны</h1>
      <NuxtImg src="http://localhost:3000/image/product_type.png" />
    </div>
    <div class="typeproduct__filter">
      <h2 class="typeproduct__filter-title">Подбор по параметрам</h2>
      <div class="typeproduct__filters">
        <UiSelector
          :options="categoryOptions"
          v-model="selectedCategory"
          placeholder="Резьба"
        />
        <UiSelector
          :options="categoryOptions"
          v-model="selectedCategory"
          placeholder="Резьба"
        />
        <UiSelector
          :options="categoryOptions"
          v-model="selectedCategory"
          placeholder="Резьба"
        />
        <UiSelector
          :options="categoryOptions"
          v-model="selectedCategory"
          placeholder="Резьба"
        />
      </div>
    </div>

    <div class="typeproduct__content">
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
          <tr class="typeproduct__content-table-table-row" v-for="item in list">
            <td class="typeproduct__content-table-td">{{ item.name }}</td>
            <td class="typeproduct__content-table-td">500</td>
            <td class="typeproduct__content-table-td">6</td>
            <td class="typeproduct__content-table-td">Нержавеющая сталь</td>
            <td class="typeproduct__content-table-td">M16*1.5</td>
            <td class="typeproduct__content-table-td">69</td>
            <td class="typeproduct__content-table-td">100</td>
            <td class="typeproduct__content-table-td">{{ item.cost }}</td>
            <td class="typeproduct__content-table-td">
              <div class="typeproduct__content-modal">
                <UiIconComents :isActive="false" @click=""></UiIconComents>
                <UiModalComments
                  @closeModal="closeModal"
                  v-if="isOpen"
                  class="typeproduct__content-table-modal-acc"
                ></UiModalComments>
              </div>
            </td>
            <td class="typeproduct__content-table-td">
              <div class="counter">
                <UiCounter></UiCounter>
              </div>
            </td>
            <td class="typeproduct__content-table-td">
              <div class="typeproduct__content-table-buttons">
                <button class="typeproduct__content-table-button">
                  В корзину
                </button>
                <button class="typeproduct__content-table-favorite">
                  <UiIconFavorites></UiIconFavorites>
                </button>
              </div>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.counter {
  display: flex;
  width: 100%;
  justify-content: center;
}
.typeproduct {
  &__content {
    margin-bottom: 130px;
    &-table {
      border-collapse: collapse;
      width: 100%;
      &-modal {
        position: relative;
        &-acc {
          position: absolute;
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

      border: 1px solid #d9d9d9;
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
