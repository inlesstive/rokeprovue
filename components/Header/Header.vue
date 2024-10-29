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
                            Производство
                        </NuxtLink>
                    </li>
                    <li class="header__top-bar-list-item">
                        <NuxtLink to="/about">
                            Оплата/Доставка
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
                <div class="header__bottom-popup">
                    <NuxtLink to="/about">
                        PDF-каталог
                    </NuxtLink>
                    <button>
                        Каталог
                    </button>
                </div>
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
                                <UiIconUser></UiIconUser>
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
.header{
    &__nav {
        border: 0.5px solid #D9D9D9;
        border-top: 0;
        display: flex;
        &-side {
            width: 100%
        }
        &-logo {
            padding: 30px 60px;
            border: 0.5px solid #D9D9D9;
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
        }
        &-bar {
            display: flex;
            border: 1px solid #D9D9D9;
            border-top: 0;
            &-list {
                display: flex;
                height: 71px;
                border: 1px solid #D9D9D9;
                border-top: 0;
                align-items: center;
                gap: 105px;
                padding: 0 30px;
                &-item {

                    & a {
                    color: #17172D;
                    font-family: "Myriad Pro";
                    font-size: 18px;
                    font-style: normal;
                    font-weight: 400;
                    line-height: 90%; 
                }
                }
            }
        }
    }
    &__bottom-bar {
        display: flex;
    }
}

</style>