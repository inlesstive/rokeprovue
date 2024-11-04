<template>
    <section class="favorites container" v-if="hasItems">
        <div class="favorites__header">
            <h2 class="favorites__title">
                Избранное
            </h2>
            <button class="favorites__clear-button">
                Очистить избранное
            </button>
        </div>
        
        <div class="favorites__section">
            <table class="favorites__table" >
                <thead class="favorites__table-header">
                    <tr class="favorites__table-row">
                        <th class="favorites__table-header-item ">Товар</th>
                        <th class="favorites__table-header-item ">Описание</th>
                        <th class="favorites__table-header-item ">Комментарий</th>
                        <th class="favorites__table-header-item"> Количество</th>
                        <th class="favorites__table-header-item ">Цена</th>
                        <th class="favorites__table-header-item ">Купить</th>
                    </tr>
                </thead>
                <tbody class="favorites__table-body" >
                    <tr class="favorites__table-row" v-for="_ in 3">
                        <td class="favorites__product-name">
                            <button class="favorites__delete">
                                <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 20 20" fill="none">
                                    <path d="M0.189743 0.391988L0.283446 0.283446C0.62702 -0.0601288 1.16465 -0.0913545 1.5435 0.189743L1.65204 0.283446L10 8.63097L18.348 0.283446C18.7259 -0.0944772 19.3386 -0.0944772 19.7165 0.283446C20.0945 0.661369 20.0945 1.27412 19.7165 1.65204L11.369 10L19.7165 18.348C20.0601 18.6915 20.0914 19.2292 19.8102 19.608L19.7165 19.7165C19.373 20.0601 18.8354 20.0914 18.4565 19.8102L18.348 19.7165L10 11.369L1.65204 19.7165C1.27412 20.0945 0.661369 20.0945 0.283446 19.7165C-0.0944772 19.3386 -0.0944772 18.7259 0.283446 18.348L8.63097 10L0.283446 1.65204C-0.0601288 1.30847 -0.0913545 0.77084 0.189743 0.391988Z" fill="#212121"/>
                                </svg>
                            </button>
                            <span class="favorites__product-name--span">
                                Шаровый гидравлический кран
                            </span>
                        </td>
                        <td class="favorites__product-description">
                            <ul class="favorites__description-list">
                                <li class="favorites__description-item">
                                    <span class="favorites__description-label">Артикул:</span>
                                    KHB-M16
                                </li>
                                <li class="favorites__description-item">
                                    <span class="favorites__description-label">Материал:</span>
                                    Нержавеющая сталь
                                </li>
                            </ul>
                        </td>
                        <td class="favorites__comment">
                            <textarea class="favorites__comment-input" placeholder="Максимум знаков: 150" maxlength="150"></textarea>
                        </td>
                        <td class="favorites__counter">
                            <div class="favorites__counter-button">
                                <UiCounter></UiCounter>
                            </div>
                        </td>
                        <td class="favorites__sum">
                            <span >
                                500 ₽
                            </span>
                        </td>
                        <td class="favorites__buyer">
                            <UiButtonSendButton class="favorites__byer-button">Добавить в корзину</UiButtonSendButton>
                        </td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>
    <section class="favorites__second container" v-else>
        <div class="favorites__second-block">
            <h2 class="favorites__second-title">
                Вы не добавили ни одного товара
            </h2>
            <span class="favorites__second-subtitle">
                Подберите интересующие вас товары в разделе каталог
            </span>
            <UiButtonSendButton class="favorites__second-button">Перейти в каталог</UiButtonSendButton>
        </div>
    </section>
</template>

<script lang="ts">
import { UiButtonSendButton } from '#build/components';

export default {
    setup() {
        const hasItems = ref(false);

        return {
            hasItems,
        };
    },
};
    
</script>

<style lang="scss">

.favorites{
    &__second{
        &-subtitle{
            color: #000;
            font-family: "Myriad Pro";
            font-size: 20px;
            font-style: normal;
            font-weight: 400;
            line-height: 100%; 
            margin-bottom: 20px;
        }
        &-title{
            color: #000;
            font-family: "Myriad Pro";
            font-size: 40px;
            font-style: normal;
            font-weight: 400;
            line-height: 90%; 
            margin-bottom: 10px;
        }
    display: flex;
    justify-content: center;
    padding-top: 329px;
    padding-bottom: 329px;
        &-block{
            display: flex;
            flex-direction: column;
            align-items: center;
        }
    }
    &__second-button{
        text-transform: none;
        width: max-content !important;
        font-size: 18px;
    }
    padding-top: 30px;
    padding-bottom: 30px;
    &__comment{
        height: 100%;
        border: 1px solid #D9D9D9;
        padding: 10px;
        &-input{
            width: 100%;
            height: 100%;
            border: none;       
            outline: none;      
            display: flex;
            align-items: flex-end;
            box-sizing: border-box;
            resize: none;
            overflow-y: hidden;
            background-color: transparent;
        }
    }
    &__clear-button{
        color: #3064C7;
        font-family: "Myriad Pro";
        font-size: 24px;
        font-style: normal;
        font-weight: 400;
        line-height: 100%;
        background-color: white;
        max-width: 216px;
        max-height: 24px;
        cursor: pointer;
    }
    &__title{
        color: #000;
        font-family: "Century Gothic";
        font-size: 105px;
        font-style: normal;
        font-weight: 700;
        line-height: 90%; 
        text-transform: uppercase;
    }
    &__header{
        display: flex;
        justify-content: space-between;
        padding-bottom: 30px;
        align-items: flex-end;
        
    }
    &__byer-button{
        width: max-content;
        
    }
    &__buyer{
        padding: 10px;
    }
    &__sum span{
        color: #000;
        font-family: "Myriad Pro";
        font-size: 24px;
        font-style: normal;
        font-weight: 400;
        line-height: 100%; 
        display: flex;
        justify-content: center;
        align-items: center;
    }
    &__sum{
        padding: 10px;
    }

    &__counter{
        padding: 10px;
    }
    &__description-list{
        display: flex;
        flex-direction: column;
        gap: 10px;
    }
    &__description-item{
        color: #000;
        font-family: "Myriad Pro";
        font-size: 18px;
        font-style: normal;
        font-weight: 400;
        line-height: 90%;
    }
    &__description-label{
        color: #000;
        font-family: "Myriad Pro";
        font-size: 18px;
        font-style: normal;
        font-weight: 400;
        line-height: 90%; 
        opacity: 0.4;
    }
    &__product-name--span{
        width: 100%;
        text-align: center;
        color: #000;
        font-family: "Myriad Pro";
        font-size: 24px;
        font-style: normal;
        font-weight: 400;
        line-height: 100%;
        padding: 10px 20px;
    }
    &__buyer{
        border: 1px solid #D9D9D9;
    }
    &__sum{
        border: 1px solid #D9D9D9;
    }
    &__counter-button{
        display: flex;
        justify-content: center;
    }
    &__counter{
        border: 1px solid #D9D9D9;
    }
    &__product-description{
        padding: 10px 20px; 
        border: 1px solid #D9D9D9;
    }
    &__product-name{
        max-width: 520px;    
        border: 1px solid #D9D9D9;
    }
    &__table-header-item{
        color: #000;
        font-family: "Myriad Pro";
        font-size: 20px;
        font-style: normal;
        font-weight: 400;
        line-height: 90%; 
        padding: 17px;
        border: 1px solid #D9D9D9;
    }
    &__delete{
        cursor: pointer;
        background-color: white; 
        padding: 33px 21px;
        border-right: 1px solid #D9D9D9;
    }
    &__table-body{
        border: 1px solid #D9D9D9;
    }
    &__table-header{
    color: #000;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
    }

  &__table{
    width: 100%;
    height: 100%;
    background-color: white;
    border-collapse: collapse;
    border: 1px solid #d9d9d9;
  }
}
</style>