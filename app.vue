<template>
  <Body>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </Body>
</template>

<style lang="scss">
.container {
  max-width: 1840px;
  width: 100%;
  margin: 0 auto;
  padding: 0 20px;
}

@media screen and (max-width: 375.99px) {
  .container {
    padding: 0 10px;
  }
}

@media screen and (max-width: 319.99px) {
}
</style>
