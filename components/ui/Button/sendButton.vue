<template>
  <button class="button">
    <slot>Отправить</slot>
  </button>
</template>

<<<<<<< HEAD
<style >
.button{
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    background: #3064C7;
    border-radius: 3px;
    width: 100%;
    color:#FFF;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 600;
    line-height: 90%; 
    text-transform: uppercase;
    padding: 20px;
=======
<style scoped>
.button {
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  background: #3064c7;
  border-radius: 3px;
  width: 100%;
  color: #fff;
  font-family: "Myriad Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 600;
  line-height: 90%;
  text-transform: uppercase;
  padding: 20px;
>>>>>>> d7b0135efa7c096530426b7487a2819cfa225037
}

.button:hover {
  background: #133e91;
}

@media screen and (max-width: 375.99px) {
  .button {
    font-size: 18px;
    padding: 15px;
  }
}
</style>
