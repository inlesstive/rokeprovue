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

<style scoped>
.breadcrumb {
  display: flex;
  list-style: none;
  padding: 0;
  margin: 0;
}
.breadcrumb-item + .breadcrumb-item::before {
  content: " / ";
  padding: 0 5px;
  color: #6c757d;
}
.breadcrumb-item {
  color: #007bff;
}
.breadcrumb-item a {
  text-decoration: none;
  color: inherit;
}
</style>
