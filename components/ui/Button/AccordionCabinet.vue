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
  min-width: 350px;
  display: flex;
  flex-direction: column;
  gap: 30px;
}
</style>
