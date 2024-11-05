<template>
  <div class="flex container">
    <UiBreadCrumbs :crumbs="breadcrumbsData" class="breadcrumbs">
    </UiBreadCrumbs>
    <div class="section">
      <h2 class="profile__title">
        {{ breadcrumbsData[breadcrumbsData.length - 1].text }}
      </h2>
      <div class="block flex">
        <ProfileNavigation></ProfileNavigation>
        <ProfileFavorites></ProfileFavorites>
      </div>
    </div>
  </div>
</template>

<script setup>
const breadcrumbsData = [
  { text: "Профиль", to: "/" },
  { text: "Избранные", to: "/" },
];
</script>

<style lang="scss">
.block {
  margin-top: 30px;
}

.section {
  margin-top: 30px;
  margin-bottom: 30px;
  display: flex;
  flex-direction: column;
  width: 100%;
}

.profile__title {
  color: #000;
  font-family: "Century Gothic";
  font-size: 105px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%;
  text-transform: uppercase;
}

.breadcrumbs {
  display: none;
}
</style>
