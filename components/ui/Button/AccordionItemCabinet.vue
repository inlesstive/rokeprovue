<template>
  <div class="accordion-item">
    <div class="accordion-header" @click="toggle">
      <div class="desktop">
        <p class="accordion-header-order-num">Номер заказа: А-07663578</p>
        <div class="accordion-header-order-wrapper">
          <NuxtLink class="accordion-header-order-download-doc" to="/">
            Скачать документы
          </NuxtLink>
          <p class="accordion-header-order-status">
            Статус заказа:
            <span>Завершен</span>
          </p>
        </div>
      </div>
      <div class="mob">
        <p class="accordion-header-order-num">Номер заказа: А-07663578</p>
        <div class="accordion-header-order-wrapper">
          <NuxtLink class="accordion-header-order-download-doc" to="/">
            <UiButtonSendButton>Скачать документ </UiButtonSendButton>
          </NuxtLink>
          <p class="accordion-header-order-status">
            Статус заказа:
            <span>Завершен</span>
          </p>
        </div>
      </div>
      <div class="accordion-header-button-hide">
        <h3 class="accordion-title" :class="{ open: isOpen }">{{ title }}</h3>
        <span class="accordion-arrow" :class="{ open: isOpen }">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="16"
            height="10"
            viewBox="0 0 16 10"
            fill="none"
          >
            <path
              d="M15 1.5L8 8.5L1 1.5"
              :stroke="isOpen ? '#3064C7' : '#17172D'"
              stroke-width="2"
            />
          </svg>
        </span>
      </div>
    </div>
    <transition name="fade">
      <div v-if="isOpen" class="accordion-content">
        <slot></slot>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      isOpen: false,
    };
  },
  methods: {
    toggle() {
      this.isOpen = !this.isOpen;
    },
  },
};
</script>

<style lang="scss" scoped>
.accordion-item {
  border: 1px solid #d9d9d9;
}
.accordion-header {
  padding: 20px;
  cursor: pointer;
  background: #f7f7f7;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  min-width: 350px;
  &-button-hide {
    display: flex;
    gap: 10px;
  }
  &-order {
    &-wrapper {
      display: flex;
      gap: 120px;
    }
    &-download-doc {
      color: #3064c7;
      font-family: "Myriad Pro";
      font-size: 18px;
      font-style: normal;
      font-weight: 600;
      line-height: 90%;
      text-decoration-line: underline;
    }
    &-status {
      color: #000;
      font-family: "Myriad Pro";
      font-size: 20px;
      font-style: normal;
      font-weight: 400;
      line-height: 90%;
      & span {
        color: #3064c7;
        font-family: "Myriad Pro";
        font-size: 20px;
        font-style: normal;
        font-weight: 400;
        line-height: 90%;
      }
    }
    &-wrapper {
      display: flex;
      max-width: 653px;
      justify-content: space-between;
    }
    &-num {
      color: #000;
      font-family: "Myriad Pro";
      font-size: 20px;
      font-style: normal;
      font-weight: 400;
      line-height: 90%;
    }
  }
}
.accordion-title {
  color: #17172d;
  font-family: "Myriad Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 600;
  line-height: 90%;
  text-transform: uppercase;
  transition: color 0.3s ease;
}
.accordion-title.open {
  color: #3064c7;
  font-family: "Myriad Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 600;
  line-height: 90%;
  text-transform: uppercase;
}

.accordion-arrow {
  transition: transform 0.3s ease;
}

.accordion-arrow.open {
  transform: rotate(180deg);
}
.accordion-content {
  padding: 20px;
  background: #f7f7f7;
  overflow-x: auto;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
.mob {
  display: none;
}

@media screen and (max-width: 1439.99px) {
}

@media screen and (max-width: 1199.99px) {
}

@media screen and (max-width: 991.99px) {
}

@media screen and (max-width: 767.99px) {
  .accordion-title {
    display: none;
  }
  .accordion-header-order-wrapper {
    display: flex;
    flex-direction: column-reverse;
    gap: 20px;
  }
  .desktop {
    display: none;
  }
  .mob {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }
}

@media screen and (max-width: 539.99px) {
}

@media screen and (max-width: 424.99px) {
}

@media screen and (max-width: 375.99px) {
}

@media screen and (max-width: 319.99px) {
}
</style>
