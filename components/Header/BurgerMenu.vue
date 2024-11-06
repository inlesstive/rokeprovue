<script setup></script>

<template>
  <div class="header__menu">
    <span class="header__menu-list-title">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="17"
        height="18"
        viewBox="0 0 17 18"
        fill="none"
      >
        <path
          d="M8.5 14.8235C9.3284 14.8235 10 15.5346 10 16.4118C10 17.2889 9.3284 18 8.5 18C7.6716 18 7 17.2889 7 16.4118C7 15.5346 7.6716 14.8235 8.5 14.8235ZM15.5 14.8235C16.3284 14.8235 17 15.5346 17 16.4118C17 17.2889 16.3284 18 15.5 18C14.6716 18 14 17.2889 14 16.4118C14 15.5346 14.6716 14.8235 15.5 14.8235ZM1.5 14.8235C2.32843 14.8235 3 15.5346 3 16.4118C3 17.2889 2.32843 18 1.5 18C0.67157 18 0 17.2889 0 16.4118C0 15.5346 0.67157 14.8235 1.5 14.8235ZM8.5 7.41177C9.3284 7.41177 10 8.12287 10 9C10 9.87713 9.3284 10.5882 8.5 10.5882C7.6716 10.5882 7 9.87713 7 9C7 8.12287 7.6716 7.41177 8.5 7.41177ZM15.5 7.41177C16.3284 7.41177 17 8.12287 17 9C17 9.87713 16.3284 10.5882 15.5 10.5882C14.6716 10.5882 14 9.87713 14 9C14 8.12287 14.6716 7.41177 15.5 7.41177ZM1.5 7.41177C2.32843 7.41177 3 8.12287 3 9C3 9.87713 2.32843 10.5882 1.5 10.5882C0.67157 10.5882 0 9.87713 0 9C0 8.12287 0.67157 7.41177 1.5 7.41177ZM8.5 0C9.3284 0 10 0.711074 10 1.58824C10 2.4654 9.3284 3.17647 8.5 3.17647C7.6716 3.17647 7 2.4654 7 1.58824C7 0.711074 7.6716 0 8.5 0ZM15.5 0C16.3284 0 17 0.711074 17 1.58824C17 2.4654 16.3284 3.17647 15.5 3.17647C14.6716 3.17647 14 2.4654 14 1.58824C14 0.711074 14.6716 0 15.5 0ZM1.5 0C2.32843 0 3 0.711074 3 1.58824C3 2.4654 2.32843 3.17647 1.5 3.17647C0.67157 3.17647 0 2.4654 0 1.58824C0 0.711074 0.67157 0 1.5 0Z"
          fill="#3064C7"
        />
      </svg>
      <button @click="console.log('catalog')">Каталог</button>
    </span>
    <ul class="header__menu-list">
      <li class="header__menu-list-item">
        <NuxtLink to="/"> Главная </NuxtLink>
      </li>
      <li class="header__menu-list-item">
        <NuxtLink to="/about"> О компании </NuxtLink>
      </li>
      <li class="header__menu-list-item">
        <NuxtLink to="/documents"> Документы </NuxtLink>
      </li>
      <li class="header__menu-list-item">
        <NuxtLink to="/news"> Новости </NuxtLink>
      </li>
      <li class="header__menu-list-item">
        <NuxtLink to="/contacts"> Контакты </NuxtLink>
      </li>
    </ul>
    <span class="header__menu-list-title">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="19"
        height="23"
        viewBox="0 0 19 23"
        fill="none"
      >
        <path
          d="M16.3293 14.7971C17.2825 14.7971 18 15.5373 18 16.3838V17.4401C18 17.8834 17.8572 18.3188 17.5866 18.6855L17.5866 18.6855C15.9992 20.8369 13.3569 22 9.49613 22C5.6343 22 2.99441 20.8364 1.41159 18.6848L0.606072 19.2774L1.41159 18.6848C1.14221 18.3186 1 17.8842 1 17.4419V16.3838C1 15.5373 1.7176 14.7971 2.67062 14.7971H16.3293ZM9.49613 1C12.2535 1 14.4338 3.15698 14.4338 5.75103C14.4338 8.34509 12.2535 10.5021 9.49613 10.5021C6.73873 10.5021 4.5584 8.34509 4.5584 5.75103C4.5584 3.15699 6.73873 1 9.49613 1Z"
          stroke="#3064C7"
          stroke-width="2"
        />
      </svg>
      <button @click="$emit('openpopup')">Личный кабинет</button>
    </span>
    <span class="header__menu-list-title">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        width="19"
        height="17"
        viewBox="0 0 19 17"
        fill="none"
      >
        <path
          d="M8.77809 3.05391L9.49805 3.79902L10.2172 3.05309L10.9959 2.24531C10.996 2.24518 10.9962 2.24505 10.9963 2.24492C12.6006 0.584898 15.1823 0.585026 16.7864 2.2453C18.4044 3.91995 18.4045 6.64227 16.7869 8.32698C16.7865 8.32736 16.7862 8.32773 16.7858 8.32811L9.4983 15.8663L2.21448 8.3276C2.21447 8.3276 2.21447 8.32759 2.21447 8.32759C0.595171 6.65159 0.595183 3.92053 2.21447 2.24458L2.21447 2.24457C3.81509 0.587923 6.3955 0.587933 7.99608 2.24457L7.99611 2.2446L8.77809 3.05391ZM9.28301 16.089C9.28305 16.089 9.28308 16.0889 9.28312 16.0889L9.28301 16.089Z"
          stroke="#3064C7"
          stroke-width="2"
        />
      </svg>
      <NuxtLink to="/favourites"> Избранное </NuxtLink>
    </span>
    <div class="header__menu-info">
      <NuxtLink to="tel:+78123098600">+7 (812) 309-86-00</NuxtLink>
      <NuxtLink to="mailto:info@roke.com">info@roke.com</NuxtLink>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.header__menu {
  background-color: #fff;
  width: 101%;
  height: 100vh;
  top: 44px;
  left: 0;
  &-info {
    margin-top: 20px;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 10px;
    & a {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 21px;
      font-style: normal;
      font-weight: 400;
      line-height: 90%; /* 18.9px */
    }
  }
  &-list {
    display: flex;
    flex-direction: column;
    gap: 20px;
    margin: 20px 0 0 15px;
    & a {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 21px;
      font-style: normal;
      font-weight: 400;
      line-height: 90%; /* 18.9px */
    }
    &-title {
      display: flex;
      padding: 20px 10px;
      align-items: center;
      gap: 10px;
      border-bottom: 1px solid #d9d9d9;
      & a,
      button {
        color: #3064c7;
        font-family: "Myriad Pro";
        font-size: 21px;
        font-style: normal;
        font-weight: 400;
        line-height: 90%;
        background: transparent;
      }
    }
  }
}
</style>
