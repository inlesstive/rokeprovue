<script setup lang="ts">
const route = useRoute()
</script>

<template>
  <section class="news container">

      <h1 class="news_title">
        <span class="sub_title">
          Актуальные события
        </span> 
        и новинки от&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;ROKE 
      </h1>

      <div class="all_card">
        <div class="card">
          <div class="card_item">

            <span class="date">
              15.08.2024
            </span>

            <img src="/public/image/news2.png"  alt="">

            <div class="dscr">
              <span class="dscr_title">
                Получение сертификата DNV
              </span>

              <p class="dscr_info">
                Наша компания получила сертификат DNV, что подтверждает соответствие продукции требованиям стандарта для морских судов и оборудования.
              </p>
            </div>

          </div>
        </div>

        <div class="card">
          <div class="card_item">

              <span class="date">
              15.08.2024
            </span>

            <img src="/public/image/news1.png"  alt="">

            <div class="dscr">
              <span class="dscr_title">
                Наше представительство в России
              </span>

              <p class="dscr_info">
                В целях улучшения взаимодействия с нашими партнерами, сокращения логистического плеча мы открыли представительство в России.
              </p>
            </div>

          </div>
        </div>
      </div>


  </section>
</template>

<style lang="scss" scoped> 

.sub_title{
  color: var(---, #3064C7);
  font-family: "Century Gothic";
  font-size: 105px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%;
  text-transform: uppercase;
}

.news_title::before{
  width: 182px;
  height: 12px;
  content: "";
  background:#17172D;
  position: absolute;
  right: 280px;
  bottom: 7px;
}

.news_title{
  width: max-content;
  position: relative;
  display: flex;
  flex-direction: column;
  color: #17172D;
  font-family: "Century Gothic";
  font-size: 105px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%;
  text-transform: uppercase;
}

.all_card{
  margin-top: 60px;
  display: flex;
  gap: 20px;
}


.card{
  background: #F7F7F7;
  display: inline-flex;
  height: 407px;
  padding: 20px;
  flex-direction: column;
  align-items: flex-start;
  gap: 10px;
  flex-shrink: 0;
}

.card_item{
  display: flex;
  width: 573px;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  gap: 20px;
}


.dscr{
  display: flex;
  width: 85%;
  flex-direction: column;
  gap: 10px;
}

.date{
  color: #808080;
  font-family: "Myriad Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%;
}

.dscr_title{
  color: #17172D;
  font-family: "Myriad Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 600;
  line-height: 90%;
  text-transform: uppercase;
}

.dscr_info{
  color: #808080;
  font-family: "Myriad Pro";
  font-size: 20px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%; 
}

.news{
  padding: 30px 0px;
}

</style>