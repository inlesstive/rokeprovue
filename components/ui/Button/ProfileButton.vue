<template>
  <button class="button">
    <slot>личные данные</slot>
  </button>
</template>

<style lang="scss" scoped>
.button {
  padding: 20px;
  display: flex;
  color: #17172d;
  font-family: "Myriad Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 600;
  line-height: 90%;
  text-transform: uppercase;
  justify-content: flex-start;
  width: 100%;
  max-width: 296px;
  background-color: white;
  border: 1px solid #d9d9d9;
  transition: 0.3s;
  cursor: pointer;
  &:hover {
    color: white;
    background-color: #3064c7;
  }
}

@media screen and (max-width: 991.99px) {
  .button{
    font-size: 16px;
  }
}

</style>
