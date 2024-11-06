<script>
const route = useRoute();

import Accordion from "../components/ui/Button/Accordion.vue";
import AccordionItem from "../components/ui/Button/AccordionItem.vue";

export default {
  components: {
    Accordion,
    AccordionItem,
  },
};
</script>

<template>
  <section class="faq container">
    <h1 class="faq__title">
      часто&nbsp;&nbsp;&nbsp;&nbsp;задаваемые
      <span class="faq__subtitle">вопросы</span>
    </h1>

    <div class="faq__content">
      <div class="faq__list">
        <ul class="faq__items">
          <li class="faq__item">
            <UiButtonFaqButton></UiButtonFaqButton>
            <UiButtonFaqButton>Изолированные фитинги</UiButtonFaqButton>
            <UiButtonFaqButton>Трубные соединения</UiButtonFaqButton>
            <UiButtonFaqButton
              >Гидравлические фитинги и клапаны</UiButtonFaqButton
            >
            <UiButtonFaqButton>Быстроразъемные соединения</UiButtonFaqButton>
            <UiButtonFaqButton
              >Бесшовные трубы из нержавеющей стали</UiButtonFaqButton
            >
            <UiButtonFaqButton>Электромагнитные клапаны</UiButtonFaqButton>
            <UiButtonFaqButton>Цапфовый шаровой кран</UiButtonFaqButton>
            <UiButtonFaqButton>Типы заглушек для труб</UiButtonFaqButton>
            <UiButtonFaqButton
              >Угловой фитинг с наружной резьбой</UiButtonFaqButton
            >
            <UiButtonFaqButton>Двойные муфтовые соединения</UiButtonFaqButton>
            <UiButtonFaqButton
              >Рабочие характеристики клапанов и фитингов</UiButtonFaqButton
            >
          </li>
        </ul>
      </div>

      <div class="faq__payment">
        <h2 class="faq__payment-title">Оплата/Доставка</h2>

        <ul class="faq__payment-list">
          <li class="faq__payment-item">
            Как происходит покупка товара?
            <span class="faq__payment-text">
              Мы работаем только с юридическими лицами. Вы можете приобрести
              товар у нас через сайт, по телефону или по электронной почте.
              После получения реквизитов и заказа мы выставляем счет для оплаты
              и спецификацию.
            </span>
          </li>

          <li class="faq__payment-item">
            Какие у вас условия оплаты?
            <span class="faq__payment-text">
              Как правило, мы работаем по 100% предоплате, но возможны другие
              варианты оплаты, которые обсуждаются индивидуально.
            </span>
          </li>

          <li class="faq__payment-item">
            Как у вас осуществляется доставка?
            <span class="faq__payment-text">
              Для вашего удобства мы предлагаем несколько вариантов доставки
              товара:
            </span>

            <p class="faq__payment-description">
              1. Самовывоз со склада по адресу г. Санкт-Петербург, ул. Латышских
              Стрелков 27 в рабочие дни с 9.00 до 18.00
              <br />
              <br />
              2. Бесплатную доставку (кроме крупногабаритных грузов) до
              терминала ТК «Деловые линии» в Санкт-Петербурге.
              <br />
              <br />
              3. Доставку по России ТК «Деловые линии» до терминала в вашем
              городе. Срок доставки от 2 до 5 дней с момента отправки. Стоимость
              доставки оплачивается покупателем.
            </p>
          </li>

          <li class="faq__payment-item">
            Какие документы нужны для самовывоза?
            <span class="faq__payment-text">
              Документ, удостоверяющий личность, доверенность или печать
              организации.
            </span>
          </li>

          <li class="faq__payment-item">
            У вас есть гарантия?
            <span class="faq__payment-text">
              Мы предоставляем годовую гарантию на нашу продукцию.
            </span>
          </li>
        </ul>
      </div>

      <div class="faq__insulated"></div>
    </div>

    <div class="faq__mobile">
      <h2 class="faq__mobile-title">FAQ</h2>
      <Accordion class="faq__mobile-accordion">
        <AccordionItem title="Оплата/Доставка">
          <div class="faq__accordion-content">
            <div class="faq__question">
              <span class="faq__question-text">
                Как происходит покупка товара?
              </span>
              <p class="faq__answer">
                Мы работаем только с юридическими лицами. Вы можете приобрести
                товар у нас через сайт, по телефону или по электронной почте.
                После получения реквизитов и заказа мы выставляем счет для
                оплаты и спецификацию.
              </p>
            </div>

            <div class="faq__question">
              <span class="faq__question-text">
                Какие у вас условия оплаты?
              </span>
              <p class="faq__answer">
                Как правило, мы работаем по 100% предоплате, но возможны другие
                варианты оплаты, которые обсуждаются индивидуально.
              </p>
            </div>

            <div class="faq__question">
              <span class="faq__question-text">
                Как у вас осуществляется доставка?
              </span>
              <ul class="faq__answer-list">
                <li>
                  1. Самовывоз со склада по адресу г. Санкт-Петербург, ул.
                  Латышских Стрелков 27 в рабочие дни с 9.00 до 18.00
                </li>
                <li>
                  2. Бесплатную доставку (кроме крупногабаритных грузов) до
                  терминала ТК «Деловые линии» в Санкт-Петербурге.
                </li>
                <li>
                  3. Доставку по России ТК «Деловые линии» до терминала в вашем
                  городе. Срок доставки от 2 до 5 дней с момента отправки.
                  Стоимость доставки оплачивается покупателем.
                </li>
              </ul>
            </div>

            <div class="faq__question">
              <span class="faq__question-text">
                Какие документы нужны для самовывоза?
              </span>
              <p class="faq__answer">
                Документ, удостоверяющий личность, доверенность или печать
                организации.
              </p>
            </div>

            <div class="faq__question">
              <span class="faq__question-text"> У вас есть гарантия? </span>
              <p class="faq__answer">
                Мы предоставляем годовую гарантию на нашу продукцию.
              </p>
            </div>
          </div>
        </AccordionItem>
      </Accordion>
      <Accordion>
        <AccordionItem title="Изолированные фитинги"> </AccordionItem>
      </Accordion>
      <Accordion>
        <AccordionItem title="Трубные соединения"> </AccordionItem>
      </Accordion>
      <Accordion>
        <AccordionItem title="Гидравлические фитинги и клапаны">
        </AccordionItem>
      </Accordion>
      <Accordion>
        <AccordionItem title="Быстроразъемные соединения"> </AccordionItem>
      </Accordion>
      <Accordion>
        <AccordionItem title="Бесшовные трубы из нержавеющей стали">
        </AccordionItem>
      </Accordion>
      <Accordion>
        <AccordionItem title="Электромагнитные клапаны"> </AccordionItem>
      </Accordion>
      <Accordion>
        <AccordionItem title="Цапфовый шаровой кран"> </AccordionItem>
      </Accordion>
      <Accordion>
        <AccordionItem title="Типы заглушек для труб"> </AccordionItem>
      </Accordion>
      <Accordion>
        <AccordionItem title="Угловой фитинг с наружной резьбой">
        </AccordionItem>
      </Accordion>
      <Accordion>
        <AccordionItem title="Двойные муфтовые соединения"> </AccordionItem>
      </Accordion>
      <Accordion>
        <AccordionItem title="Рабочие характеристики клапанов и фитингов">
        </AccordionItem>
      </Accordion>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.faq {
  &__mobile {
    display: none;
  }
  &__title {
    padding: 30px 0;
    width: max-content;
    color: #17172d;
    font-family: "Century Gothic";
    font-size: 105px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    text-transform: uppercase;
    position: relative;
    display: flex;
    flex-direction: column;

    &::before {
      width: 199px;
      height: 12px;
      content: "";
      background: #17172d;
      position: absolute;
      right: 690px;
      bottom: 132px;
    }
  }

  &__subtitle {
    color: #3064c7;
    font-family: "Century Gothic";
    font-size: 105px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    text-transform: uppercase;
  }

  &__content {
    margin-top: 39px;
    display: flex;
    gap: 20px;
  }

  &__list {
    display: flex;
    flex-direction: column;
    flex-basis: 25%;
  }

  &__payment {
    margin-bottom: 30px;
    flex-basis: 75%;
    display: flex;
    flex-direction: column;
    padding: 30px 0 30px 30px;
    gap: 60px;

    &-title {
      color: #17172d;
      font-family: "Century Gothic";
      font-size: 70px;
      font-style: normal;
      font-weight: 700;
      line-height: 90%;
      letter-spacing: -1.4px;
      text-transform: uppercase;
    }

    &-list {
      display: flex;
      flex-direction: column;
      gap: 60px;
    }

    &-item {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 40px;
      font-style: normal;
      font-weight: 400;
      line-height: 90%;
      display: flex;
      flex-direction: column;
      gap: 20px;
    }

    &-text {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 20px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
    }
  }

  &-description {
    color: #17172d;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  &__item--active {
    color: white;
    background-color: #3064c7;
  }
}

@media screen and (max-width: 1439.99px) {
  .faq__title {
    font-size: 80px;
  }
  .faq__subtitle {
    font-size: 80px;
  }
  .faq__title::before {
    width: 148px;
    height: 9px;
    content: "";
    background: #17172d;
    position: absolute;
    right: 528px;
    bottom: 107px;
  }
}

@media screen and (max-width: 1199.99px) {
  .faq__payment {
    &-title {
      color: #17172d;
      font-family: "Century Gothic";
      font-size: 64px;
      font-style: normal;
      font-weight: 700;
      line-height: 90%;
      letter-spacing: -1.4px;
      text-transform: uppercase;
    }
    &-description {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 18px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
  }
}

@media screen and (max-width: 991.99px) {
  .faq__title {
    font-size: 72px;
  }
  .faq__subtitle {
    font-size: 72px;
  }
  .faq__title::before {
    width: 113px;
    height: 8px;
    content: "";
    background: #17172d;
    position: absolute;
    right: 486px;
    bottom: 101px;
  }
  .faq__payment {
    &-title {
      color: #17172d;
      font-family: "Century Gothic";
      font-size: 42px;
      font-style: normal;
      font-weight: 700;
      line-height: 90%;
      letter-spacing: -1.4px;
      text-transform: uppercase;
    }
    &-description {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 18px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    &-item {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 28px;
      font-style: normal;
      font-weight: 400;
      line-height: 90%;
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    &-text {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 18px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
    }
  }
}

@media screen and (max-width: 767.99px) {
  .faq {
    &__title {
      display: none;
    }
    &__content {
      display: none;
    }
    &__mobile {
      display: flex;
      flex-direction: column;
    }
    &__mobile-title {
      color: #000;
      font-family: "Century Gothic";
      font-size: 50px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%;
      letter-spacing: -1px;
      text-transform: uppercase;
      padding: 10px;
    }
    &__question {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
    &__accordion-content {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    &__question-text {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 20px;
      font-style: normal;
      font-weight: 400;
      line-height: 90%;
    }
    &__question-answer {
      color: var(---, #17172d);
      font-family: "Myriad Pro";
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
    }
    &__answer-list {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
  }
}

@media screen and (max-width: 539.99px) {
  .faq {
    &__title {
      display: none;
    }
    &__content {
      display: none;
    }
    &__mobile {
      display: flex;
      flex-direction: column;
    }
    &__mobile-title {
      color: #000;
      font-family: "Century Gothic";
      font-size: 50px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%;
      letter-spacing: -1px;
      text-transform: uppercase;
      padding: 10px;
    }
    &__question {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
    &__accordion-content {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    &__question-text {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 20px;
      font-style: normal;
      font-weight: 400;
      line-height: 90%;
    }
    &__question-answer {
      color: var(---, #17172d);
      font-family: "Myriad Pro";
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
    }
    &__answer-list {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
  }
}

@media screen and (max-width: 424.99px) {
  .faq {
    &__title {
      display: none;
    }
    &__content {
      display: none;
    }
    &__mobile {
      display: flex;
      flex-direction: column;
    }
    &__mobile-title {
      color: #000;
      font-family: "Century Gothic";
      font-size: 50px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%;
      letter-spacing: -1px;
      text-transform: uppercase;
      padding: 10px;
    }
    &__question {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
    &__accordion-content {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    &__question-text {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 20px;
      font-style: normal;
      font-weight: 400;
      line-height: 90%;
    }
    &__question-answer {
      color: var(---, #17172d);
      font-family: "Myriad Pro";
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
    }
    &__answer-list {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
  }
}

@media screen and (max-width: 375.99px) {
  .faq {
    &__title {
      display: none;
    }
    &__content {
      display: none;
    }
    &__mobile {
      display: flex;
      flex-direction: column;
    }
    &__mobile-title {
      color: #000;
      font-family: "Century Gothic";
      font-size: 50px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%;
      letter-spacing: -1px;
      text-transform: uppercase;
      padding: 10px;
    }
    &__question {
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
    &__accordion-content {
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    &__question-text {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 20px;
      font-style: normal;
      font-weight: 400;
      line-height: 90%;
    }
    &__question-answer {
      color: var(---, #17172d);
      font-family: "Myriad Pro";
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
    }
    &__answer-list {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
      display: flex;
      flex-direction: column;
      gap: 10px;
    }
  }
}
</style>
