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
  { text: "Личный кабинет", to: "/account/profile" },
  { text: "Профиль пользователя", to: "/account/personaldata" },
];
</script>

<style lang="scss" scoped>
.mob {
  display: none;
}
.block {
  margin-top: 56px;
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
  margin-top: 30px;
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
    margin-top: 15px;
  }
  .flex {
    flex-direction: column;
  }
}

@media screen and (max-width: 539.99px) {
  .profile__title {
    color: #000;
    font-family: "Century Gothic";
    font-size: 40px;
    font-style: normal;
    font-weight: 700;
    line-height: 100%;
    letter-spacing: -0.8px;
    text-transform: uppercase;
  }
  .profile__title {
    margin-top: 0px;
  }
  .breadcrumbs {
    margin: 6px 0px;
    display: block;
  }
  .profile__title {
    font-size: 40px;
  }
}

@media screen and (max-width: 424.99px) {
}
@media screen and (max-width: 375.99px) {
  .mob {
    display: flex;
    &__presonal-data {
      flex-basis: 100%;
    }
  }
  .block {
    display: none;
  }
}

.section {
  margin-top: unset;
}
</style>
