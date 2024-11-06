<script setup lang="ts">
const isOpen = ref(false);
const isOpenCatalog = ref(false);
const isOpenPopUp = ref(false);
</script>

<template>
  <header class="header container">
    <nav class="header__nav">
      <NuxtLink to="/" class="header__nav-logo">
        <NuxtImg src="/image/logo.svg" />
      </NuxtLink>
      <div class="header__nav-side">
        <div class="header__top-bar">
          <ul class="header__top-bar-list">
            <li class="header__top-bar-list-item">
              <NuxtLink to="/about"> О компании </NuxtLink>
            </li>
            <li class="header__top-bar-list-item">
              <NuxtLink to="/news"> Новости </NuxtLink>
            </li>
            <li class="header__top-bar-list-item">
              <NuxtLink to="/faq"> Вопрос/Ответ </NuxtLink>
            </li>
            <li class="header__top-bar-list-item">
              <NuxtLink to="/documents"> Документы </NuxtLink>
            </li>

            <li class="header__top-bar-list-item">
              <NuxtLink to="/contacts"> Контакты </NuxtLink>
            </li>
          </ul>
          <div class="header__top-info">
            <NuxtLink to="tel:+7 (812) 309-86-00">
              +7 (812) 309-86-00
            </NuxtLink>
            <NuxtLink to="emailto:info@roke.com"> info@roke.com </NuxtLink>
          </div>
        </div>
        <div class="header__bottom-bar">
          <ul class="header__bottom-popup">
            <li class="header__bottom-popup-item">
              <NuxtLink to="/documents"> PDF-каталог </NuxtLink>
            </li>
            <li class="header__bottom-popup-item">
              <button @click="isOpenCatalog = !isOpenCatalog">Каталог</button>
            </li>
          </ul>
          <div class="header__bottom-search">
            <input
              class="header__bottom-search-input"
              type="text"
              placeholder="Что вы хотите найти?"
              name=""
              id=""
            />
            <button class="header__bottom-search-button">
              <UiIconSearch></UiIconSearch>
            </button>
          </div>
          <div class="header__bottom-action">
            <div class="header__bottom-action-button">
              <div class="header__bottom-action-button-wrap mob-hidden">
                <NuxtLink to="/favourites">
                  <UiIconFavorites></UiIconFavorites>
                </NuxtLink>
              </div>
              <div class="header__bottom-action-button-wrap">
                <NuxtLink to="/cart">
                  <UiIconCart></UiIconCart>
                </NuxtLink>
              </div>
              <div class="header__bottom-action-button-wrap mob-2">
                <button @click="isOpen = !isOpen">
                  <div :class="`menu-icon ${isOpen ? 'active' : ''}`">
                    <span></span>
                    <span></span>
                    <span></span>
                  </div>
                </button>
              </div>
              <div class="header__bottom-action-button-wrap mob-hidden">
                <button @click="isOpenPopUp = !isOpenPopUp">
                  <UiIconUser></UiIconUser>
                </button>
              </div>
            </div>
          </div>
        </div>
      </div>
      <Transition>
        <HeaderBurgerMenu
          class="header__burger-menu"
          @openpopup="isOpenPopUp = !isOpenPopUp"
          v-if="isOpen"
        ></HeaderBurgerMenu>
      </Transition>
    </nav>
    <Transition>
      <HeaderAuthPopUp
        v-if="isOpenPopUp"
        class="header__popup"
        @popupclose="isOpenPopUp = false"
      ></HeaderAuthPopUp>
    </Transition>
    <div class="header__bottom-search mob">
      <input
        class="header__bottom-search-input"
        type="text"
        placeholder="Что вы хотите найти?"
        name=""
        id=""
      />
      <button class="header__bottom-search-button">
        <UiIconSearch></UiIconSearch>
      </button>
    </div>
  </header>
  <Transition>
    <HeaderCatalogMenu
      class="header__catalog"
      v-if="isOpenCatalog"
    ></HeaderCatalogMenu>
  </Transition>
</template>

<style lang="scss" scoped>
.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}

.header__catalog {
  position: absolute;
  z-index: 10005;
  top: 143px;
  left: 0;
}

.header__popup {
  position: absolute;
  right: 0px;

  top: 143px;
  z-index: 100500;
  margin-right: 20px;
}
.header__nav {
  position: relative;
}

.header__burger-menu {
  position: absolute;
  z-index: 5;
  left: -1px;
}

.menu-icon {
  margin: 20px auto;
  width: 20px;
  height: 14px;
  cursor: pointer;
  position: relative;
}

.menu-icon span {
  background-color: black;
  height: 2px;
  position: absolute;
  width: 100%;
  left: 0;
  transition: all 0.3s ease;
  border-radius: 10px;
}

.menu-icon span:first-child {
  top: 0;
}

.menu-icon span:nth-child(2) {
  top: 6px;
}

.menu-icon span:last-child {
  top: 12px;
}

.menu-icon.active span:nth-child(2) {
  opacity: 0;
}

.menu-icon.active span:first-child,
.menu-icon.active span:last-child {
  top: 6px;
  background-color: black;
}

.menu-icon.active span:first-child {
  transform: rotate(45deg);
}

.menu-icon.active span:last-child {
  transform: rotate(-45deg);
}

.mob {
  display: none !important ;
}

.mob-2 {
  display: none !important;
}

$maxwidthrightside: 368px;

.header {
  position: relative;
  &__nav {
    border: 1px solid #d9d9d9;
    border-top: 0;
    display: flex;
    border-right: 0;
    max-height: 143px;
    &-side {
      width: 100%;
    }
    &-logo {
      display: flex;
      align-items: center;
      padding: 0 30px;
      border: 0.5px solid #d9d9d9;
      border-bottom: 0;
      border-left: 0;
      img {
        width: clamp(73px, 15vw, 237px);
        height: auto; // для сохранения пропорций
      }
    }
  }
  &__top {
    &-info {
      display: flex;
      gap: 45px;
      align-items: center;
      flex-grow: 1;
      justify-content: center;
      max-width: $maxwidthrightside;
      width: 100%;
      & a {
        color: #17172d;
        font-family: "Myriad Pro";
        font-size: 18px;
        font-style: normal;
        font-weight: 400;
        line-height: 90%;
      }
    }
    &-bar {
      display: flex;
      border: 1px solid #d9d9d9;
      border-top: 0;
      border-left: 0;

      &-list {
        display: flex;
        height: 71px;
        border: 1px solid #d9d9d9;
        border-top: 0;
        align-items: center;
        justify-content: space-between;
        padding: 0 30px;
        border-bottom: 0;
        border-left: 0;
        width: 100%;
        &-item {
          & a {
            color: #17172d;
            font-family: "Myriad Pro";
            font-size: 18px;
            font-style: normal;
            font-weight: 400;
            line-height: 90%;
            width: max-content;
            display: block;
          }
        }
      }
    }
  }
  &__bottom {
    display: flex;
    align-items: center;

    &-search {
      border-right: 1px solid #d9d9d9;
      position: relative;
      display: flex;
      align-items: center;
      flex-grow: 1; // растягиваем search на всю ширину

      &-input {
        height: 100%;
        outline: none;
        border: none;
        width: 100%; // делаем input гибким
        padding: 0 70px 0 30px;
        color: #d9d9d9;
        font-family: "Myriad Pro";
        font-size: 18px;
        font-style: normal;
        font-weight: 400;
        line-height: 90%;
      }
      &-button {
        position: absolute;
        right: 30px;
        background: transparent;
        border: none;
        cursor: pointer;
      }
    }

    &-popup {
      display: flex;
      flex-direction: row;
      align-items: center;

      &-item {
        height: 100%;
        display: flex;
        align-items: center;
        border-right: 1px solid #d9d9d9;
        & a {
          width: max-content;
        }
      }

      & a {
        color: #17172d;
        margin: 0 30px;
        font-family: "Myriad Pro";
        font-size: 18px;
        font-style: normal;
        font-weight: 600;
        line-height: 90%;
        cursor: pointer;
      }

      & button {
        color: #17172d;
        margin: 0 48px;
        background: transparent;
        border: none;
        font-family: "Myriad Pro";
        font-size: 18px;
        font-style: normal;
        font-weight: 600;
        line-height: 90%;
        cursor: pointer;
      }
    }

    &-action {
      display: flex;
      align-items: center;
      margin-left: auto;
      max-width: $maxwidthrightside;
      width: 100%;

      &-button {
        display: flex;
        height: 100%;
        align-items: center;
        width: 100%;

        &-wrap {
          height: 100%;
          display: flex;
          align-items: center;
          justify-content: center;
          border-right: 1px solid #d9d9d9;
          flex-grow: 1;

          & a {
            padding: 0 30px;
          }

          & button {
            margin: 0 30px;
            background: transparent;
            border: none;
            outline: none;
          }
        }
      }
    }

    &-bar {
      display: flex;
      height: 70px;
    }
  }
}

@media screen and (max-width: 1439.99px) {
  .header__nav-logo {
    padding: 0 10px;
    border: 0.5px solid #d9d9d9;
    border-bottom: 0;
    border-left: 0;
  }

  $maxwidthrightside: 310px;

  .header__top-info {
    max-width: $maxwidthrightside;
  }
  .header__bottom-action {
    max-width: $maxwidthrightside;
  }

  .header__bottom-popup button {
    margin: 0 30px;
  }
  .header__bottom-popup a {
    margin: 0 15px;
  }

  .header__top-bar-list {
    padding: 0 10px;
  }
}

@media screen and (max-width: 1199.99px) {
  $maxwidthrightside: 220px;

  .header__top-info {
    max-width: $maxwidthrightside;
  }
  .header__bottom-action {
    max-width: $maxwidthrightside;
  }

  .header__top-info a:last-of-type {
    display: none;
  }

  .header__bottom-action-button-wrap button {
    margin: 0 10px;
  }
  .header__bottom-action-button-wrap a {
    padding: 0 10px;
  }
  .header__bottom-popup-item {
    & a:first-child {
      display: none;
    }
  }
}

@media screen and (max-width: 991.99px) {
  $maxwidthrightside: 190px;

  .header__top-info {
    max-width: $maxwidthrightside;
  }
  .header__bottom-action {
    max-width: $maxwidthrightside;
  }
  .header__top-bar-list {
    & li:last-child {
      display: none;
    }
  }
}

@media screen and (max-width: 767.99px) {
  .header__top-bar-list-item a {
    font-size: 16px;
  }
  .header__bottom-search-button {
    position: absolute;
    right: 15px;
    background: transparent;
    border: none;
    cursor: pointer;
  }
  .header__bottom-search-input {
    padding: 0 50px 0 30px;
  }
  .header__top-bar-list {
    display: none;
  }
  .header__top-bar {
    display: none;
  }
  .header__bottom-search {
    display: none;
  }

  .mob-hidden {
    display: none;
  }
  .mob {
    display: flex !important;
    border: 1px solid #d9d9d9;
    border-top: 0;
    padding: 15px;
  }
  .mob-2 {
    display: flex !important;
  }
  .header__bottom-search-input {
    padding: 0 50px 0 0px;
  }

  .header__bottom-bar {
    height: 44px;
  }

  .header__nav-logo {
    padding: 0 36px;
  }
  .header__popup {
    position: fixed;
    left: 0;
    top: 0;
    z-index: 1000;
    width: 100vw;
  }
}

@media screen and (max-width: 539.99px) {
  .header__bottom-popup button {
    margin: 0 15px;
  }
  .header__bottom-action-button-wrap a svg {
    width: 18px;
    height: 18px;
  }

  .header__nav-logo {
    padding: 0px 10px;
  }
}

@media screen and (max-width: 424.99px) {
}

@media screen and (max-width: 375.99px) {
}

@media screen and (max-width: 319.99px) {
}
</style>
