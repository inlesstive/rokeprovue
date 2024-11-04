<template>
  <div class="accordion-item">
    <div class="accordion-header" @click="toggle">
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

<style>
.accordion-item {
  border: 1px solid #d9d9d9;
}
.accordion-header {
  padding: 20px;
  cursor: pointer;
  background-color: #fff;
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
}
.accordion-title {
  color: #17172d;
  font-family: "Myriad Pro";
  font-size: 16px;
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
  background-color: #ffffff;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
