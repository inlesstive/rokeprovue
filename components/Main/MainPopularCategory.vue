<script setup lang="ts">
const list = ref([
  {
    text: "Шаровой кран высокого давления-BKH",
    image: "http://localhost:3000/image/1.png",
  },
  {
    text: "Трубные соединения",
    image: "http://localhost:3000/image/2.png",
  },
  {
    text: "Быстроразъемное соединение",
    image: "http://localhost:3000/image/3.png",
  },
  {
    text: "Шаровой клапан",
    image: "http://localhost:3000/image/4.png",
  },
  {
    text: "SAE фланец",
    image: "http://localhost:3000/image/5.png",
  },
]);

const currentImage = ref(list.value[0].image);
const activeIndex = ref(0);

function handleMouseOver(index: any) {
  currentImage.value = list.value[index].image;
  activeIndex.value = index;
}
</script>

<template>
  <section class="pcategory container">
    <div class="pcategory__top">
      <span class="pcategory__top-descriptor">Популярные категории</span>
      <h3 class="pcategory__top-title">
        <div class="pcategory__top-title-pos">
          <span>Ведущие</span> <br />категории &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
          сегодня
        </div>
        <div class="pcategory__top-title-pos mob">
          <span>Ведущие</span> <br />
          категории сегодня
        </div>
      </h3>
    </div>

    <div class="pcategory__content">
      <NuxtImg :src="currentImage" alt="Изображение категории" />
      <ul class="pcategory__content-list">
        <li
          v-for="(item, index) in list"
          :key="index"
          class="pcategory__content-list-item"
          @mouseover="handleMouseOver(index)"
        >
          <div class="pcategory__content-wrapper">
            <NuxtImg :src="item.image" alt="Изображение категории" />
            <span :class="{ 'active-list-item': activeIndex === index }">{{
              item.text
            }}</span>
          </div>
          <UiIconArrowP />
        </li>
      </ul>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.mob {
  display: none;
}

.active-list-item {
  color: #17172d !important;
}
.pcategory__content-wrapper img {
  display: none;
}

.pcategory {
  margin-top: 150px;
  &__content {
    margin-top: 60px;
    display: flex;
    align-items: center;
    justify-content: flex-end;
    & img {
      margin-right: 20px;
      max-width: 301px;
      max-height: 303px;
      width: 100%;
      height: 100%;
    }

    &-list {
      padding: 20px 0;
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-direction: column;
      flex-grow: 1;
      max-width: 930px;

      &-item {
        padding: 20px 0;
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        border-top: 1px solid #d9d9d9;
        cursor: pointer;
        &:last-child {
          border-bottom: 1px solid #d9d9d9;
        }
        & span {
          color: #d9d9d9;
          font-family: "Myriad Pro";
          font-size: 40px;
          font-style: normal;
          font-weight: 400;
          line-height: 90%;
          width: max-content;
          transition: 0.3s;
        }
      }
    }
  }
  &__top {
    display: flex;
    justify-content: space-between;

    &-title {
      &-pos {
        color: #17172d;
        font-family: "Century Gothic";
        font-size: 70px;
        font-style: normal;
        font-weight: 700;
        line-height: 90%;
        letter-spacing: -1.4px;
        text-transform: uppercase;
        position: relative;
        &::after {
          content: "";
          position: absolute;
          background-color: #17172d;
          width: 175px;
          height: 8px;
          left: 362px;
          bottom: 4px;
        }

        & span {
          color: #3064c7;
          font-family: "Century Gothic";
          font-size: 70px;
          font-style: normal;
          font-weight: 700;
          line-height: 90%;
          letter-spacing: -1.4px;
          text-transform: uppercase;
        }
      }
    }
    &-descriptor {
      color: #17172d;
      font-family: "Century Gothic";
      font-size: 16px;
      font-style: normal;
      font-weight: 700;
      line-height: 90%;
      text-transform: uppercase;
    }
  }
}

@media screen and (max-width: 1439.99px) {
}

@media screen and (max-width: 1199.99px) {
  .pcategory__top-title-pos {
    font-size: 56px;
    & span {
      font-size: 56px;
    }
  }
  .pcategory__top-title-pos::after {
    content: "";
    position: absolute;
    background-color: #17172d;
    width: 129px;
    height: 8px;
    left: 287px;
    bottom: 3px;
  }
  .pcategory__top {
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    gap: 10px;
  }
  .pcategory__content-list-item span {
    font-size: 26px;
  }
}

@media screen and (max-width: 991.99px) {
}

@media screen and (max-width: 767.99px) {
  .pcategory__top-title-pos::after {
    display: none;
  }
  .pcategory__top-title-pos {
    display: none;
  }
  .mob {
    display: block !important;
  }

  .pcategory__content img {
    display: none;
  }
  .pcategory__content-list-item {
    padding: 10px;
    background: #f7f7f7;
    border-top: none;
    align-items: flex-start;
    &:last-child {
      border-bottom: 0px;
    }
  }
  .pcategory__content-list-item span {
    font-size: 22px;
  }
  .pcategory__content-list-item span {
    font-size: 22px;
  }
  .pcategory__content-list {
    gap: 10px;
  }

  .pcategory__content-list-item img {
    display: block;
    max-width: 52px;
  }
  .pcategory__content-wrapper {
    display: flex;
    gap: 10px;
  }
  .pcategory__content-list-item span {
    width: unset;
  }

  .pcategory__content-list-item span {
    color: #17172d;
  }
  .pcategory__content {
    margin-top: 15px;
  }
  .pcategory__content-list-item svg {
    max-width: 14px;
    transform: rotate(270deg);
  }
}

@media screen and (max-width: 539.99px) {
  .pcategory__top-title-pos {
    font-size: 35px;
    & span {
      font-size: 35px;
    }
  }
}

@media screen and (max-width: 424.99px) {
  .pcategory__top-descriptor {
    color: #17172d;
    font-family: "Century Gothic";
    font-size: 10px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    text-transform: uppercase;
  }
  .pcategory__top-title-pos {
    font-family: "Century Gothic";
    font-size: 35px;
    font-style: normal;
    font-weight: 700;
    line-height: 100%;
    letter-spacing: -0.7px;
    text-transform: uppercase;
    & span {
      font-family: "Century Gothic";
      font-size: 35px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%;
      letter-spacing: -0.7px;
      text-transform: uppercase;
    }
  }
  .pcategory {
    margin-top: 59px;
  }
  .pcategory__content-list-item span {
    color: #17172d;
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
    max-width: 230px;
  }
  .pcategory__content-list-item {
    padding: 10px;
    background: #f7f7f7;
    border-top: none;
    align-items: flex-start;
    height: 80px;
  }
  .pcategory__content-list {
    gap: 10px;
    padding: 0 0;
  }
  .pcategory__content img {
    margin-right: 0px;
  }
}

@media screen and (max-width: 375.99px) {
}

@media screen and (max-width: 319.99px) {
}
</style>
