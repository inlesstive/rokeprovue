<template>
    <div class="footer_address">
        <NuxtLink class="tel" to='tel:+7 (812) 309-86-00'> +7 (812) 309-86-00 </NuxtLink>
        <address class="address">
            Россия, Санкт-Петербург. <br>
            ул. Латвийского Стрелкова, 27
        </address>
    </div>
</template>

<style lang='scss' scoped>
.footer_address{
    display: flex;
    flex-direction: column;
    gap: 10px;
    & .address{
    color:#808080;
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%; 
    }
    & a{
    color:#808080;
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%; 
    }
}

@media screen and (max-width: 539.99px){
    .footer_address{
        & .address{
            font-size: 16px;
        }
        & a{
            font-size: 16px;
        }
    }
}

@media screen and (max-width: 424.99px){
    .footer_address{
        & .address{
            font-size: 14px;
        }
        & a{
            font-size: 14px;
        }
    }
}

@media screen and (max-width: 375.99px) {
    .footer_address{
        & .address{
            font-size: 12px;
        }
        & a{
            font-size: 12px;
        }
    }
}



</style>