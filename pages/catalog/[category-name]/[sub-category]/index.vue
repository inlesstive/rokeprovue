<script setup>
const route = useRoute();
</script>

<template>
  <div class="subcategory container">
    <h1 class="subcategory__title">Кран шаровый</h1>

    <div class="subcategory__content">
      <div class="subcategory__content-list">
        <div class="subcategory__content-list-item" v-for="_ in 3">
          <h2 class="subcategory__content-list-item-title">Для кип</h2>
          <div class="subcategory__content-list-item-content">
            <ul class="subcategory__content-list-item-content-list hidden">
              <li
                class="subcategory__content-list-item-content-list-item"
                v-for="_ in 3"
              >
                <NuxtLink to="/catalog/123/123/123">Круглый корпус</NuxtLink>
              </li>
            </ul>
            <div class="subcategory__content-list-item-content-img">
              <NuxtImg
                src="http://localhost:3000/image/subcategory.png"
              ></NuxtImg>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="subcategory__footer">
      <div class="subcategory__footer-list">
        <div class="subcategory__footer-list-item-side">
          <h4>О продукте</h4>
        </div>
        <div class="subcategory__footer-list-item-side">
          <p>
            Основные преимущества: простота и надежность конструкции,
            высококачественные материалы и широкий выбор моделей. Их применение
            охватывает строительство, сельское хозяйство, горнодобывающую и
            лесную промышленности, заправочные станции и нефтегазовую отрасль.
          </p>
          <p>
            Гидравлические шаровые краны представляют собой разновидность
            запорной арматуры, используемую в системах высокого давления для
            управления потоком в трубопроводах.
          </p>
        </div>
      </div>
      <div class="subcategory__footer-list" v-for="_ in 3">
        <div class="subcategory__footer-list-item-side">
          <h3>/Структура шарового крана</h3>
        </div>
        <div class="subcategory__footer-list-item-side">
          <p>
            Основные преимущества: простота и надежность конструкции,
            высококачественные материалы и широкий выбор моделей. Их применение
            охватывает строительство, сельское хозяйство, горнодобывающую и
            лесную промышленности, заправочные станции и нефтегазовую отрасль.
          </p>
          <p>
            Гидравлические шаровые краны представляют собой разновидность
            запорной арматуры, используемую в системах высокого давления для
            управления потоком в трубопроводах.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.hidden {
  visibility: hidden;
  opacity: 0;
  transition: opacity 0.3s ease;
}
.subcategory {
  // .subcategory__title
  margin-top: 30px;

  &__title {
    color: #17172d;
    font-family: "Century Gothic";
    font-size: 105px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    text-transform: uppercase;
    text-align: center;
    transition: 0.3s;
  }

  // .subcategory__content

  &__content {
    margin-top: 60px;
  }

  // .subcategory__content-list

  &__content-list {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 10px;
  }

  // .subcategory__content-list-item

  &__content-list-item {
    padding: 20px;
    display: flex;
    gap: 60px;
    background: #f7f7f7;
    flex-direction: column;
    max-width: 100%;
    width: 100%;
    transition: background-color 0.3s ease;

    // Меняем цвет фона и показываем скрытый текст при наведении
    &:hover {
      background: #3064c7; // Новый цвет фона при наведении
      .subcategory__content-list-item-content-img {
        visibility: hidden;
      }
      .subcategory__content-list-item-title {
        color: #ffffff;
      }
      .hidden {
        visibility: visible;
        opacity: 1;
      }
    }
  }

  // .subcategory__content-list-item-title

  &__content-list-item-title {
    color: #17172d;

    /* Кнопка 2 */
    font-family: "Myriad Pro";
    font-size: 38px;
    font-style: normal;
    font-weight: 600;
    line-height: 100%; /* 38px */
    text-transform: uppercase;
  }

  // .subcategory__content-list-item-content

  &__content-list-item-content {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    gap: 5px;
  }

  // .subcategory__content-list-item-content-list

  &__content-list-item-content-list {
    display: flex;
    flex-direction: column;
    align-items: flex-end;
    gap: 5px;
  }

  // .subcategory__content-list-item-content-list-item

  &__content-list-item-content-list-item {
    & a {
      color: #fff;

      /* Текст 5 */
      font-family: "Myriad Pro";
      font-size: 24px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%; /* 24px */
      transition: 0.3s;
      &:hover {
        text-decoration: underline;
      }
    }
  }

  // .subcategory__content-list-item-content-img

  &__content-list-item-content-img {
    & img {
      max-width: 195px;
      max-height: 157px;
      width: 100%;
      height: 100%;
    }
  }

  // .subcategory__footer

  &__footer {
    margin-top: 150px;
    margin-bottom: 150px;
  }

  // .subcategory__footer-list

  &__footer-list {
    display: flex;
    border-bottom: 1px solid #d9d9d9;
  }

  // .subcategory__footer-list-item-side

  &__footer-list-item-side {
    flex-basis: 50%;
    display: flex;
    gap: 20px;

    padding: 30px 0;
    & h3 {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 20px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
      opacity: 0.5;
    }
    & h4 {
      color: #17172d;

      /* Дескриптор */
      font-family: "Century Gothic";
      font-size: 16px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%; /* 16px */
      text-transform: uppercase;
    }
    & p {
      flex-basis: 50%;
    }
  }
}

@media screen and (max-width: 1439.99px) {
}

@media screen and (max-width: 1199.99px) {
  .subcategory__content-list {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 10px;
  }
  .subcategory__title {
    color: #17172d;
    font-family: "Century Gothic";
    font-size: 75px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    text-transform: uppercase;
    text-align: center;
    transition: 0.3s;
  }
  .subcategory__footer-list-item-side:first-child {
    flex-basis: 30%;
  }
  .subcategory__footer-list-item-side:last-child {
    flex-basis: 70%;
  }
}

@media screen and (max-width: 991.99px) {
  .subcategory__footer-list {
    flex-direction: column;
  }
  .subcategory__footer-list-item-side {
    flex-direction: column;
  }
  .subcategory__title {
    font-size: 55px;
  }
}

@media screen and (max-width: 767.99px) {
  .hidden {
    visibility: visible !important;
    opacity: 1;
  }
  .subcategory__content-list {
    display: grid;
    grid-template-columns: repeat(1, minmax(0, 1fr));
    gap: 10px;
  }
  .subcategory__content-list-item-content-img img {
    visibility: visible;
  }
  .subcategory__content-list-item a {
    visibility: visible;
    color: #000;
  }
  .subcategory__content-list-item {
    padding: 20px;
    display: flex;
    gap: 60px;
    background: #f7f7f7;
    flex-direction: column;
    max-width: 100%;
    width: 100%;
    transition: background-color 0.3s ease;
    & a {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%; /* 16px */
    }
    // Меняем цвет фона и показываем скрытый текст при наведении
    &:hover {
      background: #f7f7f7; // Новый цвет фона при наведении
      .subcategory__content-list-item-content-img {
        visibility: hidden;
      }
      .subcategory__content-list-item-title {
        color: #000;
      }
    }
  }
}

@media screen and (max-width: 539.99px) {
  .subcategory__title {
    font-size: 45px;
  }
  .profile__navigation[data-v-062f0fcd] {
    display: flex;
    flex-basis: 100%;
    gap: 30px;
    flex-direction: column;
  }
}

@media screen and (max-width: 424.99px) {
  .subcategory__title {
    font-size: 35px;
  }
}

@media screen and (max-width: 375.99px) {
}

@media screen and (max-width: 319.99px) {
}
</style>
