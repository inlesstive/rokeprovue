<script setup lang="ts">

const list = ref([
  {
    "text": 'Шаровой кран высокого давления-BKH',
    "image": 'http://localhost:3000/image/1.png'
  },
  {
    "text": 'Трубные соединения',
    "image": 'http://localhost:3000/image/2.png'
  },
  {
    "text": 'Быстроразъемное соединение',
    "image": 'http://localhost:3000/image/3.png'
  },
  {
    "text": 'Шаровой клапан',
    "image": 'http://localhost:3000/image/4.png'
  },
  {
    "text": 'SAE фланец',
    "image": 'http://localhost:3000/image/5.png'
  }
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
        Ведущие <br />
        <span>категории &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;сегодня</span>
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
          <span :class="{ 'active-list-item': activeIndex === index }">{{ item.text }}</span>
          <UiIconArrowP />
        </li>
      </ul>
    </div>
  </section>
</template>

<style lang="scss" scoped> 


.active-list-item {
  color: #17172D !important;
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
        border-top: 1px solid  #d9d9d9;
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
        color:  #3064C7;
        font-family: "Century Gothic";
        font-size: 70px;
        font-style: normal;
        font-weight: 700;
        line-height: 90%; 
        letter-spacing: -1.4px;
        text-transform: uppercase;
        & span {
          color: var(---, #17172D);
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
            background-color: #17172D;
            width: 214px;
            height: 8px;
            right: 277px;
            bottom: 14px;
          }
        }
    }
    &-descriptor {
      color: #17172D;
      font-family: "Century Gothic";
      font-size: 16px;
      font-style: normal;
      font-weight: 700;
      line-height: 90%;
      text-transform: uppercase;
    }
    & * {
      flex-basis: 50%;
    }
  }
}

</style>