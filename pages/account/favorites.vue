<template>
  <div class="flex container">
    <UiBreadCrumbs :crumbs="breadcrumbsData" class="breadcrumbs">
    </UiBreadCrumbs>
    <h2 class="profile__title">
      {{ breadcrumbsData[breadcrumbsData.length - 1].text }}
    </h2>
    <ProfileNavigation></ProfileNavigation>
    <ProfileFavorites></ProfileFavorites>
  </div>
</template>

<script setup>

const breadcrumbsData = [
  { text: 'Профиль', to: '/'},
  { text: 'Избранные', to: '/'},
]
</script>

<style lang="scss">
.breadcrumbs{
  display: none;
}

</style>