<template>
  <div class="accordion">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "Accordion",
};
</script>

<style>
.accordion {
  width: 100%;
}
</style>
