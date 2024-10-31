<script setup lang="ts">
</script>

<template>
    <button>
        <slot />
    </button>
</template>

<style lang="scss" scoped> 
button {
    color:  #17172D;
    font-family: "Myriad Pro";
    font-size: 16px;
    font-style: normal;
    font-weight: 600;
    line-height: 100%; /* 16px */
    text-transform: uppercase;
    border-radius: 3px;
    background:  #FFF;
    display: flex;
    justify-content: center;
    padding: 19px 17px;
    width: 100%;
    transition: 0.3s;
    &:hover {
        color: #D9D9D9;
    }
}

</style>