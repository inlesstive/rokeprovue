<script setup lang="ts">
const route = useRoute();
</script>

<template>
  <section class="news">
    <div class="news_top container">
      <div class="left_block">
        <p class="number">15.08.2024</p>
      </div>

      <div class="right_block">
        <h1 class="title">Получение сертификата DNV</h1>

        <h5 class="sub_title">
          Наша компания получила сертификат DNV, что подтверждает соответствие
          продукции требованиям стандарта для морских судов и оборудования.
        </h5>
      </div>
    </div>
    <NuxtImg src="http://localhost:3000/image/news.png"></NuxtImg>

    <div class="news_middle container">
      <div class="left_block">
        <p class="certificate">о сертификате</p>
      </div>

      <div class="right_block">
        <h3 class="second_title">
          Компания roke получила престижный сертификат DNV
        </h3>

        <h5 class="second_sub_title">
          Компания XYZ успешно прошла сертификацию DNV, подтвердив своё
          соответствие высшим стандартам качества и безопасности. Сертификат,
          выданный DNV, свидетельствует о высоком уровне управления качеством и
          безопасности на всех этапах производственного процесса.
        </h5>

        <h5 class="second_sub_title">
          Сертификат DNV (Det Norske Veritas) является одним из самых уважаемых
          и признанных стандартов в мире, подтверждающим соответствие строгим
          требованиям по качеству, экологической безопасности и социальной
          ответственности. Получение этого сертификата свидетельствует о том,
          что компания [Название компании] отвечает всем критериям и стандартам,
          установленным международными регуляторами.
        </h5>
      </div>
    </div>

    <div class="news_bottom container">
      <div class="left_block">
        <p class="team">команда</p>
      </div>

      <div class="right_block">
        <h3 class="second_title">Благодарность команде</h3>

        <div class="inside_block">
          <h5 class="second_sub_title">
            Поздравляем всю нашу команду и благодарим наших клиентов за
            постоянное доверие и поддержку. Мы продолжаем двигаться вперед,
            стремясь к новым вершинам и достижениям!
          </h5>

          <h5 class="second_sub_title">
            Мы выражаем благодарность всем нашим сотрудникам за их усердную
            работу и вклад в достижение этой важной цели.
          </h5>
        </div>
        <img src="http://localhost:3000/image/slug_news.png" alt="" />
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.news_top {
  padding: 30px;
  justify-content: space-between;
  display: flex;
  background-image: url("http://localhost:3000/image/news.png");
  width: 100%;
  height: 777px;
  background-position: center;
}

.news {
  & img {
    display: none;
  }
}
.number {
  color: #d9d9d9;
  font-family: "Century Gothic";
  font-size: 16px;
  font-style: normal;
  font-weight: 700;
  line-height: 100%;
  text-transform: uppercase;
}

.title {
  color: #fff;
  font-family: "Century Gothic";
  font-size: 90px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%; /* 81px */
  text-transform: uppercase;
}

.sub_title {
  width: 573px;
  color: #fff;
  font-family: "Myriad Pro";
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%;
}

.right_block {
  display: flex;
  flex-direction: column;
  gap: 30px;
  flex-basis: 50%;
}
.right_block {
  flex-basis: 50%;
}

.news_middle {
  margin-top: 80px;
  display: flex;
  justify-content: space-between;
}

.second_title {
  color: #17172d;
  font-family: "Century Gothic";
  font-size: 70px;
  font-style: normal;
  font-weight: 700;
  line-height: 90%;
  letter-spacing: -1.4px;
  text-transform: uppercase;
}

.second_sub_title {
  color: #17172d;
  font-family: "Myriad Pro";
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: 100%;
}

.news_bottom {
  margin-top: 80px;
  display: flex;
  justify-content: space-between;
}

.certificate {
  color: #17172d;
  font-family: "Century Gothic";
  font-size: 16px;
  font-style: normal;
  font-weight: 700;
  line-height: 100%;
  text-transform: uppercase;
}

.team {
  color: #17172d;
  font-family: "Century Gothic";
  font-size: 16px;
  font-style: normal;
  font-weight: 700;
  line-height: 100%;
  text-transform: uppercase;
}

.inside_block {
  gap: 3px;
  display: flex;
}

.news {
  padding-bottom: 30px;
}

@media screen and (max-width: 1439.99px) {
}

@media screen and (max-width: 1199.99px) {
}

@media screen and (max-width: 991.99px) {
  .news_top {
    flex-direction: column;
  }
  .second_title {
    font-size: 55px;
  }
}

@media screen and (max-width: 767.99px) {
  .news_top {
    background-image: unset;
    height: auto;
    margin-top: 20px;
    padding: 0 20px;
  }
  .news_middle {
    margin-top: 80px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    gap: 20px;
  }
  .news {
    & img {
      display: block;
      max-height: 383px;
      object-fit: cover;
      width: 100%;
    }
  }
  .title {
    color: #17172d;
    font-size: 55px;
    margin-top: 15px;
  }
  .sub_title {
    color: #17172d;
    font-family: "Myriad Pro";
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    width: 100%;
  }
  .right_block {
    gap: 15px;
    margin-bottom: 15px;
  }
  .second_sub_title {
    font-size: 24px;
  }
  .news_bottom {
    margin-top: 80px;
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    gap: 20px;
  }
  .inside_block {
    gap: 10px;
    display: flex;
    flex-direction: column;
  }
  .certificate {
    font-size: 10px;
  }
  .team {
    font-size: 10px;
  }
}

@media screen and (max-width: 539.99px) {
  .title {
    color: #17172d;
    font-size: 39px;
    margin-top: 15px;
  }
  .second_sub_title {
    font-size: 18px;
  }
  .second_title {
    font-size: 35px;
  }
}

@media screen and (max-width: 424.99px) {
}

@media screen and (max-width: 375.99px) {
}

@media screen and (max-width: 319.99px) {
}
</style>
