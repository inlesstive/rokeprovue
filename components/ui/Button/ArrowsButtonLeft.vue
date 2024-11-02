<template>
    <button class="arrows">
        <svg width="112" height="16" viewBox="0 0 112 16" fill="none" xmlns="http://www.w3.org/2000/svg">
    <path d="M111.707 7.29289C112.098 7.68342 112.098 8.31658 111.707 8.70711L105.343 15.0711C104.953 15.4616 104.319 15.4616 103.929 15.0711C103.538 14.6805 103.538 14.0474 103.929 13.6569L109.586 8L103.929 2.34315C103.538 1.95262 103.538 1.31946 103.929 0.928932C104.319 0.538408 104.953 0.538408 105.343 0.928932L111.707 7.29289ZM66 7L111 7V9L66 9V7Z" fill="currentColor"/>
    </svg>

    </button>  
</template>

<style scoped>
.arrows{
    background-color: white;
    outline: none;
    border: none;
    cursor: pointer;
    &:disabled{
        color: #808080;
    }
}

.arrows:hover{
    color: #8f8f8f;
}
</style>
