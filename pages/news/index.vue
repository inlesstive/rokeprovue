<script setup lang="ts">
const route = useRoute();
</script>

<template>
  <section class="news container">
    <h1 class="news_title">
      <div class="news_title-pos">
        <span class="sub_title"> Актуальные события </span> <br />
        и новинки от&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ROKE
      </div>

      <div class="news_title mob">
        <span> Актуальные <br />события </span> ROKE
        <span class="sub_title desk"> Актуальные события </span>
        и новинки от&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ROKE
      </div>
    </h1>

    <div class="all_card">
      <div class="card" v-for="_ in 20">
        <div class="card_item">
          <span class="date"> 15.08.2024 </span>

          <img src="/public/image/news2.png" alt="" />

          <div class="dscr">
            <span class="dscr_title"> Получение сертификата DNV </span>

            <p class="dscr_info">
              Наша компания получила сертификат DNV, что подтверждает
              соответствие продукции требованиям стандарта для морских судов и
              оборудования.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.desk {
  display: none;
}
.sub_title {
  color: var(---, #3064c7);
  font-family: "Century Gothic";
  font-size: 105px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%;
  text-transform: uppercase;
}

.news_title::before {
  width: 182px;
  height: 12px;
  content: "";
  background: #17172d;
  position: absolute;
  right: 280px;
  bottom: 7px;
}

.mob {
  display: none;
}

.news_title {
  width: max-content;
  position: relative;
  & .news_title-pos {
    color: var(---, #17172d);
    font-family: "Century Gothic";
    font-size: 105px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    text-transform: uppercase;
  }
}

.all_card {
  margin-top: 60px;
  display: grid;
  gap: 20px;
  grid-template-columns: repeat(3, minmax(0, 1fr));
}

.card {
  background: #f7f7f7;
  display: inline-flex;
  height: auto;
  padding: 20px;
  flex-direction: column;
  align-items: flex-start;
  gap: 10px;
  flex-shrink: 0;
  border: 1px solid #d9d9d9;
}

.card_item {
  display: flex;
  width: 100%;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  gap: 20px;
  & img {
    width: 100%;
  }
}

.dscr {
  display: flex;
  width: 85%;
  flex-direction: column;
  gap: 10px;
}

.date {
  color: #808080;
  font-family: "Myriad Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%;
}

.dscr_title {
  color: #17172d;
  font-family: "Myriad Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 600;
  line-height: 90%;
  text-transform: uppercase;
}

.dscr_info {
  color: #808080;
  font-family: "Myriad Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%;
}

.news {
  padding-top: 30px;
  padding-bottom: 30px;
}

@media screen and (max-width: 1439.99px) {
  .news_title {
    & .news_title-pos {
      font-size: 85px;
    }
  }

  .mob {
    display: none;
  }

  .sub_title {
    font-size: 85px;
  }

  .all_card {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }

  .news_title::before {
    width: 160px;
    right: 220px;
    bottom: 5px;
  }
}

@media screen and (max-width: 1199.99px) {
  .mob {
    display: none;
  }

  .news_title {
    & .news_title-pos {
      font-size: 65px;
    }
  }
  .sub_title {
    font-size: 65px;
  }

  .news_title::before {
    width: 120px;
    right: 170px;
    bottom: 4px;
  }
}

@media screen and (max-width: 991.99px) {
  .dscr_title {
    font-size: 15px;
  }

  .dscr_info {
    font-size: 15px;
  }

  .date {
    font-size: 15px;
  }

  .mob {
    display: none;
  }

  .news_title {
    & .news_title-pos {
      font-size: 55px;
    }
  }
  .sub_title {
    font-size: 55px;
  }

  .news_title::before {
    height: 8px;
    width: 105px;
    right: 141px;
    bottom: 3px;
  }
}

@media screen and (max-width: 767.99px) {
  .dscr_title {
    font-size: 12px;
  }

  .dscr_info {
    font-size: 13px;
  }

  .date {
    font-size: 14px;
  }

  .news_title-pos {
    display: none;
  }

  .news_title {
    color: #000;
    font-family: "Century Gothic";
    font-size: 60px;
    font-style: normal;
    font-weight: 700;
    line-height: 100%;
    letter-spacing: -0.8px;
    text-transform: uppercase;
  }

  .news_title::before {
    display: none;
  }
  .sub_title {
    display: none !important;
  }

  .mob {
    display: block;
    & span {
      color: #3064c7;
      font-family: "Century Gothic";
      font-size: 60px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%;
      letter-spacing: -0.8px;
      text-transform: uppercase;
    }
  }
}

@media screen and (max-width: 539.99px) {
  .news_title-pos {
    display: none;
  }

  .news_title {
    color: #000;
    font-family: "Century Gothic";
    font-size: 40px;
    font-style: normal;
    font-weight: 700;
    line-height: 100%;
    letter-spacing: -0.8px;
    text-transform: uppercase;
  }

  .sub_title {
    color: #3064c7;
    font-family: "Century Gothic";
    font-size: 40px;
    font-style: normal;
    font-weight: 700;
    line-height: 100%;
    letter-spacing: -0.8px;
    text-transform: uppercase;
  }

  .news_title::before {
    display: none;
  }

  .all_card {
    gap: 10px;
    margin-top: 10px;
    grid-template-columns: repeat(1, minmax(0, 1fr));
  }

  .card {
    display: flex;
    width: 100%;
    padding: 10px;
    flex-direction: column;
    gap: 5px;
  }

  .date {
    font-size: 10px;
  }

  .card_item img {
    max-width: 218px;
  }

  .card_item {
    display: flex;
    gap: 10px;
    width: auto;
  }

  .dscr_title {
    font-size: 17px;
  }

  .dscr_info {
    width: 311px;
    font-size: 16px;
  }

  .dscr {
    width: auto;
    display: flex;
    gap: 5px;
  }

  .news {
    padding: 10px 20px;
  }

  .mob {
    & span {
      color: #3064c7;
      font-family: "Century Gothic";
      font-size: 40px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%;
      letter-spacing: -0.8px;
      text-transform: uppercase;
    }
  }
}

@media screen and (max-width: 375.99px) {
  .news_title-pos {
    display: none;
  }

  .news_title {
    color: #000;
    font-family: "Century Gothic";
    font-size: 40px;
    font-style: normal;
    font-weight: 700;
    line-height: 100%;
    letter-spacing: -0.8px;
    text-transform: uppercase;
  }

  .sub_title {
    color: #3064c7;
    font-family: "Century Gothic";
    font-size: 40px;
    font-style: normal;
    font-weight: 700;
    line-height: 100%;
    letter-spacing: -0.8px;
    text-transform: uppercase;
  }

  .news_title::before {
    display: none;
  }

  .all_card {
    gap: 10px;
    margin-top: 10px;
    grid-template-columns: repeat(1, minmax(0, 1fr));
  }

  .card {
    display: flex;
    width: 100%;
    padding: 10px;
    flex-direction: column;
    gap: 5px;
  }

  .date {
    font-size: 10px;
  }

  .card_item img {
    max-width: 218px;
  }

  .card_item {
    display: flex;
    gap: 10px;
    width: auto;
  }

  .dscr_title {
    font-size: 17px;
  }

  .dscr_info {
    width: 311px;
    font-size: 16px;
  }

  .dscr {
    width: auto;
    display: flex;
    gap: 5px;
  }

  .news {
    padding: 10px 20px;
  }

  .mob {
    & span {
      color: #3064c7;
      font-family: "Century Gothic";
      font-size: 40px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%;
      letter-spacing: -0.8px;
      text-transform: uppercase;
    }
  }
}
</style>
