<template>
  <div class="flex container">
    <UiBreadCrumbs :crumbs="breadcrumbsData" class="breadcrumbs">
    </UiBreadCrumbs>
    <h2 class="profile__title">
      {{ breadcrumbsData[breadcrumbsData.length - 1].tex }}
    </h2>
    <div>

    </div>
  </div>
</template>

<script setup>

const breadcrumbsData = [
  { text: 'Профиль', to: '/'},
  { text: 'Реквезиты', to: '/'},
]
</script>

<style lang="scss" >
.profile__title{
    color: #000;
    font-family: "Century Gothic";
    font-size: 105px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    text-transform: uppercase;

}

.breadcrumbs{
  display: none;
}

</style>