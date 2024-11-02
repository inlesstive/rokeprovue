<template>
    <button class="button">
        <span class="button_sub">
            Каталог
        </span>
        <svg width="49" height="47" viewBox="0 0 49 47" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path  d="M2.27813 41.1875L0.465628 42.9094L3.90938 46.5344L5.72187 44.8125L2.27813 41.1875ZM45.7219 6.8125C46.7229 5.86153 46.7635 4.27914 45.8125 3.27813C44.8615 2.27711 43.2791 2.23654 42.2781 3.1875L45.7219 6.8125ZM5.72187 44.8125L45.7219 6.8125L42.2781 3.1875L2.27813 41.1875L5.72187 44.8125Z" fill="currentColor"/>
            <path  d="M6 3H41C43.7614 3 46 5.23858 46 8V41" stroke="currentColor" stroke-width="5" stroke-linecap="square" stroke-linejoin="round"/>
        </svg>
    </button>
</template>

<style scoped>

.button:hover .button_sub {
  color: #808080;
}

.button:hover svg {
 color: #808080;
}

.button{
    width: 407px;
    border-radius: 5px;
    background-color: white ;
    display: flex;
    justify-content: space-between;
    padding: 20px;
    cursor: pointer;
    outline: none; 
    border: none;
    align-items: end;  
}


.button_sub{
    color: #17172D ;
    font-family: "Myriad Pro";
    font-size: 38px;
    font-style: normal;
    font-weight: 600;
    line-height: 100%; 
    text-transform: uppercase;
}

</style>
