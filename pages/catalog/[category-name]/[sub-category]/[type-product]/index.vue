<script setup>
import { ref } from "vue";

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
]);

// Переменная для отслеживания активной модалки
const activeModalId = ref(false);

const list = ref([
  { id: 1, name: "asdasd", quantity: 1, cost: 500 },
  { id: 2, name: "asdasd", quantity: 1, cost: 500 },
  { id: 3, name: "asdasd", quantity: 1, cost: 500 },
]);

// Функция для открытия или закрытия модалки
const isOpen = ref(false);

const closeModal = () => {
  isOpen.value = false;
};
</script>

<template>
  <section class="typeproduct container">
    <UiModalComments
      v-if="isOpen"
      @closeModal="closeModal"
      @click.stop
      class="typeproduct__content-table-modal-acc"
    ></UiModalComments>

    <UiBreadCrumbs :crumbs="breadcrumbsData"></UiBreadCrumbs>
    <div class="typeproduct__banner">
      <h1><span>Шаровые</span> гидравлические краны</h1>
      <NuxtImg src="http://localhost:3000/image/product_type.png" />
    </div>
    <div class="typeproduct__filter">
      <h2 class="typeproduct__filter-title">Подбор по параметрам</h2>
      <div class="typeproduct__filters">
        <UiSelector :options="categoryOptions" placeholder="Резьба" />
      </div>
      <div class="typeproduct__filters-mobile">
        <button class="typeproduct__filters-mobile-button-filter">
          Фильтры
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="13"
            height="10"
            viewBox="0 0 13 10"
            fill="none"
          >
            <path
              d="M1.24957 8.38785C1.66355 8.38785 1.99915 8.74873 1.99915 9.19393C1.99915 9.63913 1.66355 10 1.24957 10C0.835598 10 0.5 9.63913 0.5 9.19393C0.5 8.74873 0.835598 8.38785 1.24957 8.38785ZM3.35 8.71046H12.05C12.2985 8.71046 12.5 8.92713 12.5 9.19438C12.5 9.43937 12.3307 9.64184 12.1111 9.67391L12.05 9.67829H3.35C3.10147 9.67829 2.9 9.46163 2.9 9.19438C2.9 8.94939 3.06929 8.74692 3.28894 8.71485L3.35 8.71046ZM1.24957 4.19393C1.66355 4.19393 1.99915 4.5548 1.99915 5C1.99915 5.4452 1.66355 5.80607 1.24957 5.80607C0.835598 5.80607 0.5 5.4452 0.5 5C0.5 4.5548 0.835598 4.19393 1.24957 4.19393ZM3.35 4.51654H12.05C12.2985 4.51654 12.5 4.7332 12.5 5.00045C12.5 5.24544 12.3307 5.44791 12.1111 5.47998L12.05 5.48437H3.35C3.10147 5.48437 2.9 5.2677 2.9 5.00045C2.9 4.75546 3.06929 4.55299 3.28894 4.52092L3.35 4.51654ZM1.24957 0C1.66355 0 1.99915 0.360891 1.99915 0.806066C1.99915 1.25124 1.66355 1.61213 1.24957 1.61213C0.835598 1.61213 0.5 1.25124 0.5 0.806066C0.5 0.360891 0.835598 0 1.24957 0ZM3.35 0.32261H12.05C12.2985 0.32261 12.5 0.539268 12.5 0.806524C12.5 1.05151 12.3307 1.25398 12.1111 1.28602L12.05 1.29044H3.35C3.10147 1.29044 2.9 1.07378 2.9 0.806524C2.9 0.561535 3.06929 0.359071 3.28894 0.327029L3.35 0.32261Z"
              fill="white"
            />
          </svg>
        </button>
        <button class="typeproduct__filters-mobile-button-popular">
          По популярности
          <svg
            width="13"
            height="12"
            viewBox="0 0 13 12"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M2.75251 11.7475C2.8892 11.8842 3.1108 11.8842 3.24749 11.7475L5.47487 9.5201C5.61156 9.38342 5.61156 9.16181 5.47487 9.02513C5.33819 8.88844 5.11658 8.88844 4.9799 9.02513L3 11.005L1.0201 9.02513C0.883417 8.88844 0.661809 8.88844 0.525126 9.02513C0.388442 9.16181 0.388442 9.38342 0.525126 9.5201L2.75251 11.7475ZM2.65 0.5L2.65 11.5L3.35 11.5L3.35 0.5L2.65 0.5Z"
              fill="black"
            />
            <path
              d="M9.75251 0.252513C9.8892 0.115829 10.1108 0.115829 10.2475 0.252513L12.4749 2.4799C12.6116 2.61658 12.6116 2.83819 12.4749 2.97487C12.3382 3.11156 12.1166 3.11156 11.9799 2.97487L10 0.994975L8.0201 2.97487C7.88342 3.11156 7.66181 3.11156 7.52513 2.97487C7.38844 2.83819 7.38844 2.61658 7.52513 2.4799L9.75251 0.252513ZM9.65 11.5L9.65 0.5L10.35 0.5L10.35 11.5L9.65 11.5Z"
              fill="black"
            />
          </svg>
        </button>
      </div>
    </div>

    <div class="typeproduct__content">
      <UiTableTable2></UiTableTable2>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.counter {
  display: flex;
  width: 100%;
  justify-content: center;
}
.typeproduct__filters-mobile {
  display: none;
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
    overflow-x: auto;

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
      margin-top: 15px;
    }
  }
}

@media screen and (max-width: 1439.99px) {
}

@media screen and (max-width: 1199.99px) {
}

@media screen and (max-width: 991.99px) {
  .typeproduct__banner h1 {
    font-size: 87px;
    & span {
      font-size: 87px;
    }
  }
}

@media screen and (max-width: 767.99px) {
  .typeproduct__banner h1 {
    font-size: 60px;
    & span {
      font-size: 60px;
    }
  }
  .typeproduct__banner img {
    max-width: 274px;
    margin: -15px;
  }
  .typeproduct__filters {
    display: none;
  }
  .typeproduct__filter-title {
    display: none;
  }
  .typeproduct__filters-mobile {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    &-button-filter {
      display: flex;
      width: 100%;
      padding: 10px 20px;
      justify-content: center;
      align-items: center;
      gap: 5px;
      background: #3064c7;
      color: #fff;
      font-family: "Myriad Pro";
      font-size: 14px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
    }
    &-button-popular {
      display: flex;
      width: 100%;
      padding: 10px 20px;
      justify-content: center;
      align-items: center;
      gap: 5px;
      background: #fff;
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 14px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%; /* 14px */
    }
  }
}

@media screen and (max-width: 539.99px) {
  .typeproduct__banner h1 {
    font-size: 45px;
    & span {
      font-size: 45px;
    }
  }
  .typeproduct__banner img {
    max-width: 200px;
    margin: -15px;
  }
}

@media screen and (max-width: 424.99px) {
  .typeproduct__banner h1 {
    font-size: 35px;
    & span {
      font-size: 35px;
    }
  }
}

@media screen and (max-width: 375.99px) {
  .typeproduct__banner h1 {
    font-size: 30px;
    & span {
      font-size: 30px;
    }
  }
}

@media screen and (max-width: 319.99px) {
}
</style>
