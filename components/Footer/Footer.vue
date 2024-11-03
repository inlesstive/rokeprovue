<template>
    <footer class="footer container">


        <div class="footer_top">
            <div class="footer_side">
                <FooterAddress class="first_address"></FooterAddress>

                <div class="footer_side-wapper mob"> 
                    <ul class="footer-list">
                        <li class="list-item">
                            О компании
                        </li>
                        <li class="list-item">
                            Каталог
                        </li>
                        <li class="list-item">
                            Документы
                        </li>
                        <li class="list-item">
                            PDF-каталог
                        </li>
                        <li class="list-item">
                            FAQ
                        </li>
                    </ul>
                </div>

            </div>



            <div class="footer_side">
                <div class="footer-side-wrapper">
                    <ul class="footer-list">
                    <li class="list-item">
                        О компании
                    </li>
                    <li class="list-item">
                        Производство
                    </li>
                    <li class="list-item">
                        Каталог
                    </li>
                    <li class="list-item">
                        PDF-каталог
                    </li>
                    <li class="list-item">
                        Оплата/Доставка
                    </li>
                    <li class="list-item">
                        Документы
                    </li>
                    <li class="list-item">
                        Отзывы
                    </li>
                </ul>

                <ul class="footer-list">
                    <li class="list-item">
                        Новости
                    </li>
                    <li class="list-item">
                        Контакты
                    </li>
                </ul>

                </div>
                
                <div class="footer-side-wapper mob">
                    <ul class="footer-list">
                        <li class="list-item">
                            Новости
                        </li>
                        <li class="list-item">
                            Контакты
                            </li>
                        </ul>
                        <FooterAddress class="secnod_address"></FooterAddress>
                </div>

            </div>




            


        </div>


        <span class="email">
            info@roke.com
        </span>

        <div class="footer_bottom">

            <div class="political">
                <span class="political_discr">
                    Политика конфиденциальности
                </span>
                <span class="political_discr">
                    Пользовательское Соглашение
                </span>
            </div>
            <span class="political_site">
                Разработка сайта sokolagency.ru 
            </span>

        </div>

        
    </footer>
</template>


<style scoped>
.mob{
    display: none;
}

.footer-side-wrapper{
    max-width: 375px;
    display: flex;
    justify-content: space-between;
    width: 100%;
}

.list-item{
    color: #FFF;
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%; 
}

.footer-list{
    display: flex;
    flex-direction: column;
    gap: 10px;
}


.footer_top{
    width: 100%;
    display: flex;
}

.footer_side{
    display: flex;
    flex-basis: 50%;
}


.political_site{
    color: #808080;
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
}

.political_discr{
    color: #808080;
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
    text-decoration: underline;
    text-underline-offset: 3px;
    text-decoration-thickness: 1px; 
    text-decoration-color: #808080;
}




.footer{
    width: 100%;
    height: 100%;
    padding: 30px;
    align-items: center;
    flex-direction: column;
    display: flex;
    background: #17172D;
}





.email{
    margin-top: 111px;
    color: #FFF;
    font-family: "Myriad Pro";
    font-size: clamp(30px, 18vw, 331px);
    font-style: normal;
    font-weight: 400;
    line-height: 70%;
    letter-spacing: -16.55px;
}

.footer_bottom{
    margin-top: 28px;
    justify-content: space-between;
    display: flex;
    width: 100%;
    height: 100%;
}


.political{
    display: flex;
    gap: 20px;
}

@media screen and (max-width: 1439.99px) {
    
}

@media screen and (max-width: 1199.99px) {

}

@media screen and (max-width: 991.99px) {
    .email{
        font-size: clamp(30px, 17vw, 331px);
        letter-spacing: -7px;
    }



    .political{
        gap: 10px;
        flex-direction: column;
    }

}

@media screen and (max-width: 767.99px) {
    .footer_bottom {
        gap: 10px;
        margin-top: 28px;
        display: flex;
        width: 100%;
        height: 100%;
        flex-direction: column;
    }

    .political {
        display: flex;
        gap: unset;
        justify-content: space-between;
        flex-direction: row;
    }

    .political_site {
        display: flex;
        color: #808080;
        font-family: "Myriad Pro";
        font-size: 14px;
        font-style: normal;
        font-weight: 400;
        line-height: 90%;
        justify-content: flex-end;
    }


    .political_discr {
        color: #808080;
        font-family: "Myriad Pro";
        font-size: 14px;
        font-style: normal;
        font-weight: 400;
        line-height: 90%;
        text-decoration: underline;
        text-underline-offset: 3px;
        text-decoration-thickness: 1px;
        text-decoration-color: #808080;
    }


    .mob{
        display: flex;
        flex-direction: column;
        gap: 31px;
    }

    .footer-side-wrapper{
        display: none;
    }


    .first_address{
        display: none;
    }




}

@media screen and (max-width: 539.99px) {
    .list-item{
        font-size: 16px;
    }


    .political_discr {
        font-size: 13px;
    }


    .political_site {
        display: flex;
        font-size: 13px;
        justify-content: flex-end;
    }

   

    .email{
        margin-top: 30px;
    }
}

@media screen and (max-width: 424.99px) {
    .list-item{
        font-size: 14px;
    }


    .political_discr {
        font-size: 11px;
    }



    .political_site {
        display: flex;
        font-size: 11px;
        justify-content: flex-end;
    }



    .email{
        margin-top: 30px;
    }
}

@media screen and (max-width: 375.99px) {

    .footer_top{
        padding: 20px 10px 30px 10px;
    }

    .mob{
        display: flex;
        flex-direction: column;
        gap: 31px;
    }

    .footer-side-wrapper{
        display: none;
    }


    .political_discr {
        font-size: 10px;
    }


    .list-item{
        font-size: 14px;
    }

    .political_site {
        display: flex;
        font-size: 10px;
        justify-content: flex-end;
    }



    .first_address{
        display: none;
    }



    .footer {
    padding: 10px;
    }



    .email{
        margin-top: 30px;
        letter-spacing: -4px;
    }
}

@media screen and (max-width: 319.99px) {
    
}
</style>