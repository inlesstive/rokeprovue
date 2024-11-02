<script setup lang="ts">
const route = useRoute();
</script>

<template>
  <section class="about">
    <h1 class="about_title">
      <span class="sub_title"> Roke: Надежные <br /> </span>
      Промышленные &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;решения
    </h1>
    <h1 class="about_title mob container">
      <span class="sub_title"> Roke: Надежные <br /> </span>
      Промышленные решения
    </h1>

    <div class="about_top">
      <NuxtImg src="http://localhost:3000/image/about.png" />
      <div class="about_top-line-l">
        <div class="about_top-line"></div>
      </div>
      <div class="about_top-info">
        <span>
          Мы гарантируем надежность и долговечность нашей продукции, обеспечивая
          бесперебойную работу ваших систем.
        </span>
      </div>
    </div>

    <div class="about_middle container">
      <div class="decision">
        <div class="dec">
          <p class="title">о нас</p>
        </div>

        <div class="all_dscr">
          <h2 class="decision_title">
            <span class="decision_sub_title"> ROKE Fluid: лучшие <br /> </span>
            Решения для &nbsp;&nbsp;&nbsp;Индустрии
          </h2>
          <h2 class="decision_title mob">
            <span class="decision_sub_title"> ROKE Fluid: </span> лучшие<br />
            Решения для Индустрии
          </h2>

          <div class="dsc_top">
            <span class="dscr">
              Компания ROKE Fluid, основанная в 2008 году в городе Наньтун,
              провинции Хайнань, производит высококачественные фитинги, муфты и
              гидравлические соединения. Наша команда высококвалифицированных
              сотрудников удовлетворяет потребности различных отраслей
              промышленности.
            </span>

            <span class="dscr">
              Наша продукция используется в нефтяной, химической,
              металлургической, энергетической промышленности, атомной
              энергетике и судостроении. Изделия ROKE Fluid предназначены для
              работы в условиях высоких и сверхвысоких температур, давления и
              коррозионной активности, что делает их идеальными для тяжелых
              условий эксплуатации.
            </span>
          </div>
        </div>
      </div>

      <div class="equipment">
        <span class="number">01</span>

        <div class="block">
          <span class="equipment_title">Современное оборудование</span>

          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="17"
            height="17"
            viewBox="0 0 17 17"
            fill="none"
          >
            <circle cx="8.5" cy="8.5" r="8.5" fill="#17172D" />
          </svg>
        </div>
      </div>

      <div class="card">
        <div class="card__spacer"></div>
        <ul class="list">
          <li class="list_item">Широкий и современный парк оборудования</li>
          <li class="list_item">Обучение в ведущих мировых компаниях</li>
          <li class="list_item">Станки ЧПУ</li>
          <li class="list_item">Оборудование для 3D-моделирования</li>
          <li class="list_item">Контроль химического состава сырья</li>
        </ul>
      </div>

      <div class="equipment">
        <span class="number">02</span>

        <div class="block">
          <span class="equipment_title">Комплексные Инженерные Услуги</span>

          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="17"
            height="17"
            viewBox="0 0 17 17"
            fill="none"
          >
            <circle cx="8.5" cy="8.5" r="8.5" fill="#17172D" />
          </svg>
        </div>
      </div>

      <div class="card">
        <div class="card__spacer"></div>
        <ul class="list">
          <li class="list_item">Более чем 40 патентов на изобретения</li>
          <li class="list_item">Высокотехнологичное предприятие Китая</li>
          <li class="list_item">Изготовление по индивидуальны чертежам</li>
        </ul>
      </div>

      <div class="equipment">
        <span class="number">03</span>

        <div class="block">
          <span class="equipment_title">Индивидуальный подход</span>

          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="17"
            height="17"
            viewBox="0 0 17 17"
            fill="none"
          >
            <circle cx="8.5" cy="8.5" r="8.5" fill="#17172D" />
          </svg>
        </div>
      </div>

      <div class="card">
        <div class="card__spacer"></div>
        <ul class="list">
          <li class="list_item">Поддержка на Всех Этапах</li>
          <li class="list_item">Индивидуальные Консультации</li>
          <li class="list_item">Постоянное Сотрудничество</li>
          <li class="list_item">Гибкие Условия Сотрудничества</li>
        </ul>
      </div>
    </div>

    <div class="about_footer container">
      <div class="footer_decision">
        <div class="footer_dec">
          <p class="footer_title">мы в цифрах</p>
        </div>

        <div class="all_dscr">
          <h2 class="footer_decision_title">
            <span class="footer_decision_sub_title"> Глобальное </span>
            Расширение и &nbsp;&nbsp;&nbsp;Качество
          </h2>
          <h2 class="footer_decision_title mob">
            <span class="footer_decision_sub_title"> Глобальное </span> <br />
            Расширение и Качество
          </h2>

          <div class="footer_block">
            <span class="dscr">
              Наша продукция экспортируется более чем в 100 стран, включая
              Соединенные Штаты, Японию, Германию, Южную Америку, Юго-Восточную
              Азию. В 2023 году мы открыли официальное представительство в
              России, что соответствует нашему плану развития на ближайшие 10
              лет
            </span>

            <span class="dscr">
              Наша компания прошла сертификацию CCS, CE, продукция соответствует
              всем необходимым международным стандартам, включая стандарты
              ANSI/ASME, DIN, BS, JIS, GB, CB и других серий.
            </span>
          </div>

          <div class="footer_info">
            <div class="footer_card_up">
              <div class="footer_card">
                <span class="footer_card-item"> Персонал </span>

                <p class="quantity">Более 100 человек</p>
              </div>

              <div class="footer_card">
                <span class="footer_card-item"> Сертификат </span>

                <p class="quantity">ISO9001-2008</p>
              </div>
            </div>

            <div class="footer_card_bottom">
              <div class="footer_card">
                <span class="footer_card-item"> Площадь завода </span>

                <p class="quantity">5 000  м²</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.sub_title {
  color: #3064c7;
  font-family: "Century Gothic";
  font-size: 105px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%;
  text-transform: uppercase;
  width: max-content;
}

.about_top-info {
  position: absolute;
  top: 0;
  padding: 20px;
  z-index: 10002;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;

  & span {
    background-color: #fff;
    max-width: 483px;
    height: max-content;
    color: #17172d;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    padding: 20px;
    margin-left: 400px;
    margin-top: 55px;
  }
}

.mob {
  display: none !important;
}
.about_middle {
  margin-top: 84px;
}
.about_top-line {
  position: relative;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  &::before {
    position: absolute;
    content: "";
    width: 2px;
    height: 100%;
    background-color: #fff;
  }
}
.about_top-line-l {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
}
.about_top {
  position: relative;
  margin-top: 30px;

  &::after {
    position: absolute;
    content: "";
    width: 100%;
    height: 2px;
    background: #fff;
    top: 120px;
    left: 0;
  }
  &::before {
    position: absolute;
    content: "";
    width: 2px;
    height: 100%;
  }
}
.about_top img {
  width: 100%;
  object-fit: cover;
  max-width: 100%;
  height: 705px;
}

.about_title {
  width: max-content;
  position: relative;
  color: #17172d;
  font-family: "Century Gothic";
  font-size: 105px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%;
  text-transform: uppercase;
  padding: 0 20px;
}

.about_title::before {
  width: 218px;
  height: 14px;
  content: "";
  background: #17172d;
  position: absolute;
  right: 452px;
  bottom: 7px;
}

.title {
  color: #17172d;
  font-family: "Century Gothic";
  font-size: 16px;
  font-style: normal;
  font-weight: 700;
  line-height: 100%;
  text-transform: uppercase;
}

.about_middle {
  padding: 10px;
  display: flex;
  flex-direction: column;
}

.decision_title {
  align-content: end;
  width: max-content;
  position: relative;

  color: #17172d;
  font-family: "Century Gothic";
  font-size: 70px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%;
  letter-spacing: -1.4px;
  text-transform: uppercase;
}

.decision_sub_title {
  color: #3064c7;
  font-family: "Century Gothic";
  font-size: 70px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%;
  letter-spacing: -1.4px;
  text-transform: uppercase;
}

.decision_title::before {
  width: 85px;
  height: 8px;
  content: "";
  background: #17172d;
  position: absolute;
  right: 395px;
  bottom: 5px;
}

.dscr {
  color: #000;
  font-family: "Myriad Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%;
  width: 455px;
  display: flex;
}

.all_dscr {
  display: flex;
  gap: 20px;
  flex-direction: column;
}

.dec {
  display: flex;
  justify-content: space-between;
}

.equipment {
  align-items: center;
  display: flex;
  justify-content: space-between;
  padding: 20px;
  background: #f7f7f7;
}

.number {
  color: #000;
  font-family: "Myriad Pro";
  font-size: 30px;
  font-style: normal;
  font-weight: 400;
  line-height: 90%;
  flex-basis: 50%;
}

.equipment_title {
  color: #000;
  font-family: "Myriad Pro";
  font-size: 30px;
  font-style: normal;
  font-weight: 400;
  line-height: 90%;
}

.list {
  display: flex;
  flex-direction: column;
  align-content: flex-end;
  flex-basis: 50%;
  gap: 10px;
  margin-top: 20px;
  margin-bottom: 30px;
}

.card__spacer {
  flex-basis: 50%;
}
.list_item {
  color: #000;
  font-family: "Myriad Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%;
  list-style-type: disc;
  list-style-position: inside;
}

.card {
  margin-left: auto;
  margin-right: 250px;
  width: 100%;
  display: flex;
}

.decision {
  gap: 29px;
  display: flex;
  margin-bottom: 30px;
  justify-content: space-between;
}

.block {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-basis: 50%;
}

.footer_decision {
  gap: 20px;
  justify-content: space-between;
  display: flex;
}

.footer_dec {
  display: flex;
  gap: 715px;
}

.footer_title {
  color: #000;
  font-family: "Myriad Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 600;
  line-height: 90%;
  text-transform: uppercase;
}

.footer_decision_title {
  display: flex;
  width: max-content;
  position: relative;
  flex-direction: column;
  color: #17172d;
  font-family: "Century Gothic";
  font-size: 70px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%;
  letter-spacing: -1.4px;
  text-transform: uppercase;
}

.footer_decision_sub_title {
  color: #3064c7;
  font-family: "Century Gothic";
  font-size: 70px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%;
  letter-spacing: -1.4px;
  text-transform: uppercase;
}

.footer_decision_title::before {
  width: 85px;
  height: 8px;
  content: "";
  background: #17172d;
  position: absolute;
  right: 340px;
  bottom: 5px;
}

.footer_info {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.footer_card {
  margin-top: 40px;
  display: flex;
  flex-direction: column;
  width: 100%;
}

.footer_card-item {
  color: #808080;
  font-family: "Myriad Pro";
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%;
  padding-bottom: 10px;
  border-bottom: 1px solid;
  border-color: #808080;
}

.quantity {
  padding-top: 20px;
  color: #000;
  font-family: "Myriad Pro";
  font-size: 40px;
  font-style: normal;
  font-weight: 400;
  line-height: 90%;
  letter-spacing: -2px;
}

.footer_card_up {
  display: flex;
  gap: 20px;
}

.footer_card_bottom {
  display: flex;
  width: 50%;
}

.footer_block {
  display: flex;
  gap: 20px;
}

.dsc_top {
  display: flex;
  gap: 20px;
}

.about {
  padding-bottom: 100px;
  padding-top: 30px;
}

@media screen and (max-width: 1799.99px) {
  .about_title {
    font-size: 92px;
    & span {
      font-size: 92px;
    }
  }
  .about_title::before {
    width: 206px;
    height: 14px;
    content: "";
    background: #17172d;
    position: absolute;
    right: 397px;
    bottom: 7px;
  }
}

@media screen and (max-width: 1439.99px) {
  .about_title {
    font-size: 70px;
    & span {
      font-size: 70px;
    }
  }
  .about_title::before {
    width: 158px;
    height: 9px;
    content: "";
    background: #17172d;
    position: absolute;
    right: 302px;
    bottom: 5px;
  }
}

@media screen and (max-width: 1199.99px) {
  .about_title {
    font-size: 62px;
    & span {
      font-size: 62px;
    }
  }
  .decision_title {
    font-size: 62px;
    & span {
      font-size: 62px;
    }
  }
  .footer_decision_sub_title {
    font-size: 62px;
  }
  .footer_decision_title {
    font-size: 62px;
  }
  .about_title::before {
    width: 141px;
    height: 9px;
    content: "";
    background: #17172d;
    position: absolute;
    right: 267px;
    bottom: 5px;
  }
  .footer_decision {
    flex-wrap: wrap;
  }
}

@media screen and (max-width: 991.99px) {
  .about_title {
    font-size: 46px;
    & span {
      font-size: 46px;
    }
  }
  .decision_title {
    font-size: 46px;
    & span {
      font-size: 46px;
    }
  }
  .footer_decision_sub_title {
    font-size: 46px;
  }
  .footer_decision_title {
    font-size: 46px;
  }
  .about_title::before {
    width: 105px;
    height: 7px;
    content: "";
    background: #17172d;
    position: absolute;
    right: 199px;
    bottom: 3px;
  }
  .decision {
    flex-direction: column;
  }
  .footer_block {
    flex-wrap: wrap;
  }
  .dscr {
    width: 100%;
  }
}

@media screen and (max-width: 767.99px) {
  .about_title::before {
    display: none;
  }
  .about_title {
    width: unset;
    display: none;
  }
  .mob {
    display: block !important;
  }
  .footer_decision_title {
    width: 100%;
  }
  .footer_decision_title::before {
    display: none;
  }
  .about_top-info span {
    background-color: #fff;
    max-width: 483px;
    height: -moz-max-content;
    height: max-content;
    color: #17172d;
    font-family: "Myriad Pro";
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    padding: 20px;
    margin-left: unset;
    margin-top: unset;
  }
  .about_top-line-l {
    display: none;
  }
  .about_top::after {
    display: none;
  }
  .footer_card-item {
    border-bottom: unset;
  }
  .about_top-info {
    position: absolute;
    top: 0;
    padding: 0;
    padding-bottom: 20px;
    z-index: 10002;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: flex-start;
    flex-direction: row;
    align-items: flex-end;
  }
  .footer_card_bottom {
    width: 100%;
  }
  .footer_card {
    border: 1px solid #d9d9d9;
    padding: 15px;
    margin-top: 0;
  }
  .footer_card_up {
    flex-wrap: wrap;
  }
  .about_top img {
    height: 340px;
  }
  .dsc_top {
    display: flex;
    gap: 20px;
    flex-direction: column;
  }
  .dscr {
    width: unset;
  }
  .decision_title {
    display: none;
    width: unset;
  }
  .decision_title::before {
    display: none;
  }
  .card__spacer {
    display: none;
  }
  .list {
    flex-basis: 100%;
  }
  .number {
    flex-basis: unset;
  }
  .block {
    flex-basis: 100%;
  }
  .block {
    & svg {
      display: none;
    }
  }
  .equipment {
    gap: 10px;
  }
  .footer_decision_title {
    display: none;
  }
}

@media screen and (max-width: 539.99px) {
  .about_title {
    font-size: 39px;
    & span {
      font-size: 39px;
    }
  }
  .decision_title {
    font-size: 39px;
    & span {
      font-size: 39px;
    }
  }
  .footer_decision_sub_title {
    font-size: 39px;
  }
  .footer_decision_title {
    font-size: 39px;
  }
  .about_top-info span {
    font-size: 10px;
    max-width: 165px;
    padding: 10px;
  }
  .list_item {
    font-size: 16px;
  }
  .equipment_title {
    font-size: 20px;
  }
  .number {
    font-size: 20px;
  }
  .dscr {
    font-size: 18px;
  }
}

@media screen and (max-width: 424.99px) {
}

@media screen and (max-width: 375.99px) {
}

@media screen and (max-width: 319.99px) {
}
</style>
