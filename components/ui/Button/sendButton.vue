<template>

    <button class="button">
        <slot>Отправить</slot>
    </button>

</template>

<style scoped>
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
}


.button:hover{
    background: #133E91;
}

</style>