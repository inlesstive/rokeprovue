<template>
  <nav aria-label="breadcrumb">
    <ol class="breadcrumb">
      <li v-for="(crumb, index) in crumbs" :key="index" class="breadcrumb-item">
        <NuxtLink v-if="!isLast(index)" :to="crumb.to">{{
          crumb.text
        }}</NuxtLink>
        <span v-else>{{ crumb.text }}</span>
      </li>
    </ol>
  </nav>
</template>

<script setup>
import { computed } from "vue";
import { defineProps } from "vue";

const props = defineProps({
  crumbs: {
    type: Array,
    required: true,
    default: () => [],
  },
});

const isLast = (index) => index === props.crumbs.length - 1;
</script>

<style lang="scss" scoped>
.breadcrumb {
  display: flex;
  list-style: none;
  flex-wrap: wrap;
  padding: 0;
  margin: 0;
}
.breadcrumb-item + .breadcrumb-item::before {
  content: " // ";
  padding: 0 5px;
  color: #d9d9d9;
}
.breadcrumb-item {
  color: #d9d9d9;
  & span {
    color: #17172d;
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
  }
}
.breadcrumb-item a {
  text-decoration: none;
  color: inherit;
  transition: 0.3s;
  color: #d9d9d9;

  font-family: "Myriad Pro";
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: 90%; /* 16.2px */
  &:hover {
    color: #17172d;
  }
}
</style>
