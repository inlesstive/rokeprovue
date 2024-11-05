<template>
  <div class="flex container">
    <UiBreadCrumbs :crumbs="breadcrumbsData" class="breadcrumbs">
    </UiBreadCrumbs>
    <h2 class="profile__title">
      {{ breadcrumbsData[breadcrumbsData.length - 1].tex }}
    </h2>
    <ProfileNavigation></ProfileNavigation>
    <ProfilePresonalData></ProfilePresonalData>
  </div>
</template>

<script setup>

const breadcrumbsData = [
  { text: 'Профиль', to: '/'},
  { text: 'Личные данные', to: '/'},
]
</script>

<style lang="scss">
.breadcrumbs{
  display: none;
}

</style>