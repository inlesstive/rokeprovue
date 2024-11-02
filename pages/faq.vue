<script setup lang="ts">
const route = useRoute()


</script>

<template>
  <section class="FaQ container">

    <h1 class="title">
      часто&nbsp;&nbsp;&nbsp;&nbsp;задаваемые
      <span class="sub_title">вопросы</span>
    </h1>

    <div class="faq-content"> 

      <div class="faq-list">
        <ul class="list">
          <li class="list-item"> 
            <UiButtonFaqButton ></UiButtonFaqButton>
            <UiButtonFaqButton >Изолированные фитинги</UiButtonFaqButton>
            <UiButtonFaqButton>Трубные соединения</UiButtonFaqButton>
            <UiButtonFaqButton>Гидравлические фитинги и клапаны</UiButtonFaqButton>
            <UiButtonFaqButton>Быстроразъемные соединения</UiButtonFaqButton>
            <UiButtonFaqButton>Бесшовные трубы из нержавеющей стали</UiButtonFaqButton>
            <UiButtonFaqButton>Электромагнитные клапаны</UiButtonFaqButton>
            <UiButtonFaqButton>Цапфовый шаровой кран</UiButtonFaqButton>
            <UiButtonFaqButton>Типы заглушек для труб</UiButtonFaqButton>
            <UiButtonFaqButton>Угловой фитинг с наружной резьбой</UiButtonFaqButton>
            <UiButtonFaqButton>Двойные муфтовые соединения</UiButtonFaqButton>
            <UiButtonFaqButton>Рабочие характеристики клапанов и фитингов</UiButtonFaqButton>
          </li>
        </ul>
      </div>

      <div class="payment-content_block" >
         <h2 class="payment-title">
          Оплата/Доставка
         </h2>

         <ul class="payment-list">

            <li class="payment-list_item">
              Как происходит покупка товара?
              <span class="item-text">
                Мы работаем только с юридическими лицами. Вы можете приобрести товар у нас через сайт, по телефону или по электронной почте. После получения реквизитов и заказа мы выставляем счет для оплаты и спецификацию.
              </span>
            </li>

            <li class="payment-list_item">
              Какие у вас условия оплаты?
              <span class="item-text">
                Как правило, мы работаем по 100% предоплате, но возможны другие варианты оплаты, которые обсуждаются индивидуально.
              </span>
            </li> 
            
            <li class="payment-list_item">
              Как у вас осуществляется доставка?
              <span class="item-text">
                Для вашего удобства мы предлагаем несколько вариантов доставки товара:  
              </span>

              <p class="item-dscr">
                1. Самовывоз со склада по адресу г. Санкт-Петербург, ул. Латышских Стрелков 27 в рабочие дни с 9.00 до 18.00
                <br>
                <br>
                2. Бесплатную доставку (кроме крупногабаритных грузов) до терминала ТК «Деловые линии» в Санкт-Петербурге. 
                <br>
                <br>
                3. Доставку по России ТК «Деловые линии» до терминала в вашем городе. Срок доставки от 2 до 5 дней с момента отправки. Стоимость доставки оплачивается покупателем.
              </p>
            </li>

            <li class="payment-list_item">
              Какие документы нужны для самовывоза?
              <span class="item-text">
                Документ, удостоверяющий личность, доверенность или печать организации.
              </span>
            </li> 

            <li class="payment-list_item">
              У вас есть гарантия?
              <span class="item-text">
                Мы предоставляем годовую гарантию на нашу продукцию.
              </span>
            </li> 

         </ul>
      </div>

      <div class="insulated-content_block" >
      </div>

    </div>


  </section>
</template>

<style lang="scss" scoped> 
.payment-title{
  color: var(---, #17172D);
  font-family: "Century Gothic";
  font-size: 70px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%; 
  letter-spacing: -1.4px;
  text-transform: uppercase;
}

.item-dscr{
  color: #17172D;
  font-family: "Myriad Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%; 
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.payment-list{
  display: flex;
  flex-direction: column;
  gap: 60px;  
}

.item-text{
  color: #17172D;
  font-family: "Myriad Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%; 
}

.payment-list_item{
  color: #17172D;
  font-family: "Myriad Pro";
  font-size: 40px;
  font-style: normal;
  font-weight: 400;
  line-height: 90%;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.payment-content_block{
  margin-bottom: 30px;
  display: flex;
  flex-direction: column;
  padding: 30px 0px 30px 30px;
  gap: 60px;
}

.faq-content{
  margin-top: 39px;
  display: flex;
  gap: 20px;
}

.active {
  color: white;
  background-color: #3064C7;
}

.title{
  padding: 30px 0px;
  width: max-content;
  color: #17172D;
  font-family: "Century Gothic";
  font-size: 105px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%; 
  text-transform: uppercase;
  position: relative;
  display: flex;
  flex-direction: column;
}

.title::before{
  width: 199px;
  height: 12px;
  content: "";
  background:#17172D;
  position: absolute;
  right: 690px;
  bottom: 132px;
}

.sub_title{
  color: #3064C7;
  font-family: "Century Gothic";
  font-size: 105px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%; 
  text-transform: uppercase;
}

</style>