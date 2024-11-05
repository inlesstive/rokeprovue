<template>
  <section class="container">
    <div class="flex">
      <UiBreadCrumbs :crumbs="breadcrumbsData" class="breadcrumbs">
      </UiBreadCrumbs>
      <div class="section">
        <h2 class="profile__title">
          {{ breadcrumbsData[breadcrumbsData.length - 1].text }}
        </h2>
        <div class="block flex">
          <ProfileNavigation></ProfileNavigation>
          <ProfilePresonalData></ProfilePresonalData>
        </div>
        <div class="mob">
          <ProfilePresonalData class="mob__presonal-data"></ProfilePresonalData>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const breadcrumbsData = [
  { text: "Профиль", to: "/" },
  { text: "Профиль пользователя", to: "/" },
];
</script>

<style lang="scss">
.mob {
  display: none;
}
.block {
  margin-top: 30px;
  display: flex;
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

@media screen and (max-width: 375.99px) {
.profile__title{
    font-size: 40px;
}
  .mob {
    display: flex;
    &__presonal-data {
      flex-basis: 100%;
    }
  }
  .breadcrumbs{
    margin: 15px 0px;
    display: block;
  }
  .block {
    display: none;
  }
}
.flex{
    flex-direction: column;
}
.section{
    margin-top: unset;
}
</style>
