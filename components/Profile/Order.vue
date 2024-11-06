<template>
  <div class="order">
    <UiButtonAccordionCabinet class="order__accordion">
      <div class="profile__section-table-wrapper" v-for="_ in 5">
        <span>23 февраля 2024</span>
        <UiButtonAccordionItemCabinet class="order__item" title="Свернуть">
          <table class="order__table">
            <thead>
              <tr>
                <th class="order__table-header">Наименование товара</th>
                <th class="order__table-header">Описание</th>
                <th class="order__table-header">Количество</th>
                <th class="order__table-header">Сумма</th>
              </tr>
            </thead>
            <tbody>
              <tr class="order__row" v-for="_ in 10">
                <td class="order__product-name">Шаровый гидравлический кран</td>
                <td class="order__product-description">
                  <ul class="order__description-list">
                    <li class="order__description-item">
                      <span class="order__description-label">Артикул:</span>
                      KHB-M16
                    </li>
                    <li class="order__description-item">
                      <span class="order__description-label">Материал:</span>
                      Нержавеющая сталь
                    </li>
                  </ul>
                </td>
                <td class="order__quantity">1 000</td>
                <td class="order__sum">500 000 ₽</td>
              </tr>
            </tbody>
          </table>
          <div class="order__summary">
            <span class="order__total-label"
              >Товаров на сумму: 1 500 000 ₽</span
            >
            <h3 class="order__total-heading">Итого: 1 500 000 ₽</h3>
          </div>
        </UiButtonAccordionItemCabinet>
      </div>
    </UiButtonAccordionCabinet>
  </div>
</template>

<style lang="scss" scoped>
.order {
  flex-basis: 85%;
  &__accordion {
    max-width: 1563px;
  }
  &__table {
    width: max-content;
    background-color: white;
    border-collapse: collapse;
    border: 1px solid #d9d9d9;
  }
  &__table-header {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 600;
    line-height: 90%;
    padding: 17px 20px;
    border: 1px solid #d9d9d9;
  }
  &__item {
    width: 100%;
  }
  &__product-name {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    padding: 10px 20px;
    border: 1px solid #d9d9d9;
  }
  &__description-label {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
    opacity: 0.4;
  }
  &__product-description {
    border: 1px solid #d9d9d9;
  }
  &__description-item {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
  }
  &__description-list {
    padding: 10px 20px;
    display: flex;
    flex-direction: column;
    gap: 10px;
  }
  &__quantity {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 600;
    line-height: 90%;
    padding: 10px;
    border: 1px solid #d9d9d9;
    text-align: center;
  }
  &__sum {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    padding: 10px;
    border: 1px solid #d9d9d9;
    text-align: center;
  }
  &__summary {
    display: flex;
    justify-content: space-between;
    margin-top: 20px;
    flex-wrap: wrap;
    gap: 10px;
  }
  &__total-label {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
  }
  &__total-heading {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 38px;
    font-style: normal;
    font-weight: 600;
    line-height: 100%;
  }
}
</style>
