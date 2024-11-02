<script setup lang="ts">
</script>

<template>
  <section class="main__hero">
    <NuxtImg src="http://localhost:3000/hero.png"/>
    
      <div class="main__hero-info">
        <div class="">
          <h1 class="main__hero-info-title">
          <div class="main__hero-info-title-pos">
            <span>Компоненты</span> гидравлики: <br> надежность &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; и качество!
          </div>
          <div class="main__hero-info-title-pos mob">
            <span>Компоненты</span> гидравлики:  надежность и качество!
          </div>  
          
        </h1>
        <p class="main__hero-info-descr">
          Мы предоставляем качественные комплектующие для гидравлических систем и трубопроводов, обеспечивая надежность и доступность нашей продукции как на складах в России, так и под заказ в любом объеме.
        </p>
        </div>

      <UiButton class="main__hero-info-button"></UiButton>
      <div class="main__hero-info-button-mob">
        <MainHeroBtn >Каталог</MainHeroBtn>
      </div>
      </div>

      
    
  </section>
</template>

<style lang="scss" scoped> 


.main__hero-info-button-mob {
  display: none;
}

.main__hero {
  margin-top: 25px;
  position: relative;
  &-info {
    position: absolute;
    top: 0;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    &-button {
      margin-left: auto;
      margin-right: 323px;
      margin-bottom: 20px;
    }
    &-descr {
      max-width: 407px;
      background: #fff;
      padding: 0 20px 20px 20px;
      margin-left: auto;
      margin-right: 323px;
      color: var(---, #17172D);


      font-family: "Myriad Pro";
      font-size: 20px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%;
    }
    &-title {

      background-color: #fff;
      padding: 6px 20px 31px 20px;
      &-pos {
        position: relative;
        color:  #17172D;
        font-family: "Century Gothic";
        font-size: 105px;
        font-style: normal;
        font-weight: 700;
        line-height: 90%;
        text-transform: uppercase;
        width: max-content;

        &::after {
          content: "";
          position: absolute;
          width: 309px;
          height: 12px;
          z-index: 100010;
          background: #17172D;
          bottom: 7px;
          left: 703px;

          
        }
      }
      & span {
        color:  #3064C7;

        font-family: "Century Gothic";
        font-size: 105px;
        font-style: normal;
        font-weight: 700;
        line-height: 90%; 
        text-transform: uppercase;
      }
    }
  }
  & img {
    width: 100%;
    height: auto;
    min-height: 590px;
    max-height: 907px;
    object-fit: cover;
  }
}

.mob {
  display: none;
}

@media screen and (max-width: 1709.99px) {
    .main__hero-info-title-pos {
        font-size: 87px ;
    }
    .main__hero-info-title span {
          font-size: 87px ;
      }
      .main__hero-info-title-pos::after {
          width: 249px;
          left: 583px;
      }
  }

  @media screen and (max-width: 1439.99px) {
    .main__hero-info-title-pos {
        font-size: 69px ;
    }
    .main__hero-info-title span {
          font-size: 69px ;
      }
      .main__hero-info-title-pos::after {
          width: 196px;
          left: 465px;
          bottom: 5px;
      }
  }
  
  @media screen and (max-width: 1199.99px) {
    .main__hero-info-title-pos {
        font-size: 57px ;
    }
    .main__hero-info-title span {
          font-size: 57px ;
      }
      .main__hero-info-title-pos::after {
          width: 160px;
          left: 384px;
          bottom: 5px;
          height: 9px;
      }
  }
  
  @media screen and (max-width: 991.99px) {
    .main__hero-info-title-pos {
        font-size: 39px ;
    }
    .main__hero-info-title span {
          font-size: 39px ;
      }
      .main__hero-info-title-pos::after {
          width: 111px;
          left: 263px;
          bottom: 3px;
          height: 6px;
      }
      .main__hero-info-title {
          
          top: 0;
          background-color: #fff;
          padding: 6px 20px 15px 20px;
      }
  }
  
  @media screen and (max-width: 767.99px) {
    .main__hero-info-title-pos::after {
      display: none;
    }
    .main__hero-info-title-pos {
      display: none;
      max-width: 276px;
    }
    .mob {
      display: block !important;
    }
    .main__hero-info-title {
          
          top: 0;
          background-color: #fff;
          padding: 10px 20px 10px 10px;
          width: fit-content;
    }
    .main__hero-info-descr {
      color:  #17172D;
      font-family: "Myriad Pro";
      font-size: 10px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%; 
      margin-right: unset;
      padding: 0 10px 10px 10px;
      margin-left: unset;
      max-width: 242px;
    }
    .main__hero-info-button {
      display: none;
    }

    .main__hero {
        margin-top: 0;
    }
    .main__hero-info-title-pos {
      line-height: 95%;
    }
    .main__hero-info {
        width: 100%;
    }
    .main__hero-info-button-mob {
      display: block;
      margin: 0 10px 15px 10px;
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