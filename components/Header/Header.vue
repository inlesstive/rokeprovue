<script setup lang="ts">
defineProps<{
  disabled?: boolean,
}>()
</script>


<template>
    <header class="header container">
        <nav class="header__nav">
            <div class="header__nav-logo">
                <NuxtImg src="/image/logo.svg" />
            </div>
            <div class="header__nav-side">
                <div class="header__top-bar">
                <ul class="header__top-bar-list">
                    <li class="header__top-bar-list-item">
                        <NuxtLink to="/about">
                            О компании
                        </NuxtLink>
                    </li>
                    <li class="header__top-bar-list-item">
                        <NuxtLink to="/about">
                            Новости
                        </NuxtLink>
                    </li>
                    <li class="header__top-bar-list-item">
                        <NuxtLink to="/about">
                            Вопрос/Ответ
                        </NuxtLink>
                    </li>
                    <li class="header__top-bar-list-item">
                        <NuxtLink to="/about">
                            Документы
                        </NuxtLink>
                    </li>

                    <li class="header__top-bar-list-item">
                        <NuxtLink to="/about">
                            Контакты
                        </NuxtLink>
                    </li>
                </ul>
                <div class="header__top-info">
                    <NuxtLink to="/about">
                            +7 (812) 309-86-00
                    </NuxtLink>
                    <NuxtLink to="/about">
                            info@roke.com
                    </NuxtLink>
                </div>
            </div>
            <div class="header__bottom-bar">
                <ul class="header__bottom-popup">
                    <li class="header__bottom-popup-item">
                        <NuxtLink to="/about">
                            PDF-каталог
                        </NuxtLink>
                    </li>
                    <li class="header__bottom-popup-item">
                        <button>
                            Каталог
                        </button>
                    </li>
                </ul>
                <div class="header__bottom-search">
                    <input class="header__bottom-search-input" type="text" placeholder="Что вы хотите найти?" name="" id="">
                    <button class="header__bottom-search-button">
                        <UiIconSearch></UiIconSearch>
                    </button>
                </div>
                <div class="header__bottom-action">
                    <div class="header__bottom-action-button">
                        <div class="header__bottom-action-button-wrap">
                            <NuxtLink to="/about">
                                <UiIconFavorites></UiIconFavorites>
                            </NuxtLink>
                        </div>
                        <div class="header__bottom-action-button-wrap">
                            <NuxtLink to="/about">
                                <UiIconCart></UiIconCart>
                            </NuxtLink>
                        </div>
                        <div class="header__bottom-action-button-wrap">
                            <button>
                                <UiIconUser disabled="true"></UiIconUser>
                            </button>
                        </div>

                    </div>
                </div>
            </div>
            </div>

        </nav>
    </header>
</template>

<style lang="scss" scoped>



$maxwidthrightside: 368px;

.header{
    &__nav {
        border: 1px solid #D9D9D9;
        border-top: 0;
        display: flex;
        border-right: 0;
        max-height: 143px;
        &-side {
            width: 100%
        }
        &-logo {
            display: flex;
            align-items: center;
            padding: 0 30px;
            border: 0.5px solid #D9D9D9;
            border-bottom: 0;
            border-left: 0;
            img {
                width: clamp(73px, 15vw, 237px); 
                height: auto; // для сохранения пропорций
            }
        }
    }
    &__top {
        &-info {
            display: flex;
            gap: 45px;
            align-items: center;
            flex-grow: 1;
            justify-content: center;
            max-width: $maxwidthrightside;
            width: 100%;
            & a {
                color: #17172D;
                font-family: "Myriad Pro";
                font-size: 18px;
                font-style: normal;
                font-weight: 400;
                line-height: 90%; 
            }
        }
        &-bar {
            display: flex;
            border: 1px solid #D9D9D9;
            border-top: 0;
            border-left: 0;
            
            &-list {
                display: flex;
                height: 71px;
                border: 1px solid #D9D9D9;
                border-top: 0;
                align-items: center;
                justify-content: space-between;
                padding: 0 30px;
                border-bottom: 0;
                border-left: 0;
                width: 100%;
                &-item {

                    & a {
                        color: #17172D;
                        font-family: "Myriad Pro";
                        font-size: 18px;
                        font-style: normal;
                        font-weight: 400;
                        line-height: 90%; 
                        width: max-content;
                        display: block;
                    }
                }
            }
        }
    }
    &__bottom {
        display: flex;
        align-items: center;


    &-search {
        border-right: 1px solid #D9D9D9;
        position: relative;
        display: flex;
        align-items: center;
        flex-grow: 1; // растягиваем search на всю ширину

        &-input {
            height: 100%;
            outline: none;
            border: none;
            width: 100%; // делаем input гибким
            padding: 0 70px 0 30px;
            color: #D9D9D9;
            font-family: "Myriad Pro";
            font-size: 18px;
            font-style: normal;
            font-weight: 400;
            line-height: 90%;
        }
        &-button {
            position: absolute;
            right: 30px;
            background: transparent;
            border: none;
            cursor: pointer;
        }
    }

    &-popup {
        display: flex;
        flex-direction: row;
        align-items: center;

        &-item {
            height: 100%;
            display: flex;
            align-items: center;
            border-right: 1px solid #D9D9D9;
            & a {
                width: max-content;
            }
        }

        & a {
            color: #17172D;
            margin: 0 30px;
            font-family: "Myriad Pro";
            font-size: 18px;
            font-style: normal;
            font-weight: 600;
            line-height: 90%;
            cursor: pointer;
        }

        & button {
            color: #17172D;
            margin: 0 48px;
            background: transparent;
            border: none;
            font-family: "Myriad Pro";
            font-size: 18px;
            font-style: normal;
            font-weight: 600;
            line-height: 90%;
            cursor: pointer;
        }
    }

    &-action {
        display: flex;
        align-items: center;
        margin-left: auto; 
        max-width: $maxwidthrightside;
        width: 100%;

        &-button {
            display: flex;
            height: 100%;
            align-items: center;
            width: 100%;

            &-wrap {
                height: 100%;
                display: flex;
                align-items: center;
                justify-content: center;
                border-right: 1px solid #D9D9D9;
                flex-grow: 1;

                & a {
                    padding: 0 30px;
                }

                & button {
                    margin: 0 30px;
                    background: transparent;
                    border: none;
                    outline: none;
                }
            }
        }
    }

    &-bar {
        display: flex;
        height: 70px;
    }
}

}



@media screen and (max-width: 1439.99px) {
    .header__nav-logo {
        padding: 0 10px;
        border: 0.5px solid #D9D9D9;
        border-bottom: 0;
        border-left: 0;
    }

    $maxwidthrightside: 310px;

    .header__top-info {
        max-width: $maxwidthrightside;
    }
    .header__bottom-action {
        max-width: $maxwidthrightside;
    }

    .header__bottom-popup button {
        margin: 0 30px;
    }
    .header__bottom-popup a {
        margin: 0 15px;
    }

    .header__top-bar-list {
        padding: 0 10px;

    }
}

@media screen and (max-width: 1199.99px) {
    $maxwidthrightside: 220px;

    .header__top-info {
        max-width: $maxwidthrightside;
    }
    .header__bottom-action {
        max-width: $maxwidthrightside;
    }

    .header__top-info a:last-of-type {
        display: none;
    }

    .header__bottom-action-button-wrap button {
        margin: 0 10px;
    }
    .header__bottom-action-button-wrap a {
        padding: 0 10px;
    }
    .header__bottom-popup-item {
        & a:first-child {
            display: none;
        }
    }
}

@media screen and (max-width: 991.99px) {
    $maxwidthrightside: 190px;

    .header__top-info {
        max-width: $maxwidthrightside;
    }
    .header__bottom-action {
        max-width: $maxwidthrightside;
    }
    .header__top-bar-list {
        & li:last-child {
            display: none;
        }
    }
}

@media screen and (max-width: 767.99px) {
    .header__top-bar-list-item a {
        font-size: 16px;

    }
    .header__bottom-search-button {
        position: absolute;
        right: 15px;
        background: transparent;
        border: none;
        cursor: pointer;
    }
    .header__bottom-search-input {
        padding: 0 50px 0 30px;
    }
    .header__top-bar-list {
        display: none;
    }
}

@media screen and (max-width: 539.99px) {
    
}

@media screen and (max-width: 424.99px) {
    
}

@media screen and (max-width: 375.99px) {
    
}

@media screen and (max-width: 319.99px) {
    
}
</style>