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
        <ProfileDetails></ProfileDetails>
      </div>
    </div>
  </div>
</template>

<script setup>
const breadcrumbsData = [
  { text: "Профиль", to: "/account/profile" },
  { text: "Реквезиты", to: "/account/details" },
];
</script>

<style lang="scss">
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
@media screen and (max-width: 1439.99px) {
}

@media screen and (max-width: 1199.99px) {
}

@media screen and (max-width: 991.99px) {
  .profile__title {
    font-size: 75px;
  }
}

@media screen and (max-width: 767.99px) {
  .profile__title {
    font-size: 65px;
  }
  .breadcrumbs {
    display: block;
    margin-top: 20px;
  }
  .flex {
    flex-direction: column;
  }
}

@media screen and (max-width: 539.99px) {
  .profile__title {
    font-size: 45px;
  }
}

@media screen and (max-width: 424.99px) {
}
@media screen and (max-width: 375.99px) {
  .profile__title {
    font-size: 35px;
  }
  .mob {
    display: flex;
    &__presonal-data {
      flex-basis: 100%;
    }
  }
  .breadcrumbs {
    margin: 15px 0px;
    display: block;
  }
  .block {
    display: none;
  }
}

.section {
  margin-top: unset;
}
</style>
