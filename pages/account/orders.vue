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
        <ProfileOrder></ProfileOrder>
      </div>
    </div>
  </div>
</template>

<script setup>
const breadcrumbsData = [
  { text: "Профиль", to: "/account/profile" },
  { text: "История заказов", to: "/account/orders" },
];
</script>

<style lang="scss" scoped>
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

.accordion-content {
  padding: 20px;
  background: #f7f7f7;
  overflow-x: auto !important;
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
  .breadcrumbs {
    display: block;
    margin-top: 20px;
  }
  .flex {
    display: flex;
    justify-content: space-between;
    flex-direction: column;
  }
  .profile__title {
    font-size: 65px;
  }
}

@media screen and (max-width: 539.99px) {
  .profile__title {
    color: #000;
    font-family: "Century Gothic";
    font-size: 38px;
    font-style: normal;
    font-weight: 700;
    line-height: 100%;
    letter-spacing: -0.76px;
    text-transform: uppercase;
  }
}

@media screen and (max-width: 424.99px) {
}
</style>
