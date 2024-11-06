<script setup lang="ts"></script>

<template>
  <div class="main__hits container">
    <div class="main__hits-head">
      <span class="main__hits-head-name"> Хиты продаж </span>
      <h3 class="main__hits-head-title">
        Откройте наши <br />
        <span>бестселлеры</span> для &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;себя
      </h3>
      <h3 class="main__hits-head-title mob">
        Откройте наши <br />
        <span>бестселлеры</span> <br />
        для себя
      </h3>
    </div>
    <div class="main__hits-card-list">
      <div class="main__hits-card-list-item">
        <h4 class="main__hits-card-list-item-title">
          /Внутренний поперечный шаровой кран 2000 фунтов на квадратный дюйм
        </h4>
        <div class="main__hits-card-list-item-img">
          <NuxtImg
            src="https://roke.pro/_next/image?url=%2Fmain%2Fbestseller1.png&w=640&q=75"
          />
        </div>
        <div class="main__hits-card-list-item-bottom">
          <span>PN 500 / DN 06</span>
          <span>500 RUB</span>
        </div>
      </div>
      <div class="main__hits-card-list-item">
        <h4 class="main__hits-card-list-item-title">
          /Внутренний поперечный шаровой кран 2000 фунтов на квадратный дюйм
        </h4>
        <div class="main__hits-card-list-item-img">
          <NuxtImg
            src="https://roke.pro/_next/image?url=%2Fmain%2Fbestseller1.png&w=640&q=75"
          />
        </div>
        <div class="main__hits-card-list-item-bottom">
          <span>PN 500 / DN 06</span>
          <span>500 RUB</span>
        </div>
      </div>

      <div class="main__hits-card-list-p">
        Высококачественные комплектующие для гидравлических систем, проверенные
        временем и которым доверяют профессионалы.
      </div>
      <div class="main__hits-card-list-item">
        <h4 class="main__hits-card-list-item-title">
          /Внутренний поперечный шаровой кран 2000 фунтов на квадратный дюйм
        </h4>
        <div class="main__hits-card-list-item-img">
          <NuxtImg
            src="https://roke.pro/_next/image?url=%2Fmain%2Fbestseller1.png&w=640&q=75"
          />
        </div>
        <div class="main__hits-card-list-item-bottom">
          <span>PN 500 / DN 06</span>
          <span>500 RUB</span>
        </div>
      </div>
      <div class="main__hits-card-list-item">
        <h4 class="main__hits-card-list-item-title">
          /Внутренний поперечный шаровой кран 2000 фунтов на квадратный дюйм
        </h4>
        <div class="main__hits-card-list-item-img">
          <NuxtImg
            src="https://roke.pro/_next/image?url=%2Fmain%2Fbestseller1.png&w=640&q=75"
          />
        </div>
        <div class="main__hits-card-list-item-bottom">
          <span>PN 500 / DN 06</span>
          <span>500 RUB</span>
        </div>
      </div>
      <div></div>
      <div class="main__hits-card-list-item">
        <h4 class="main__hits-card-list-item-title">
          /Внутренний поперечный шаровой кран 2000 фунтов на квадратный дюйм
        </h4>
        <div class="main__hits-card-list-item-img">
          <NuxtImg
            src="https://roke.pro/_next/image?url=%2Fmain%2Fbestseller1.png&w=640&q=75"
          />
        </div>
        <div class="main__hits-card-list-item-bottom">
          <span>PN 500 / DN 06</span>
          <span>500 RUB</span>
        </div>
      </div>
      <div class="main__hits-card-list-item-bordered">
        <span>
          ПОСМОТРЕТЬ БОЛЬШЕ
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="15"
            height="14"
            viewBox="0 0 15 14"
            fill="none"
          >
            <path
              d="M1.32428 11.2628L0.587121 11.9386L1.93857 13.4129L2.67572 12.7372L1.32428 11.2628ZM14.6757 1.73715C15.0828 1.36396 15.1103 0.731394 14.7372 0.324275C14.364 -0.0828437 13.7314 -0.110347 13.3243 0.262846L14.6757 1.73715ZM2.67572 12.7372L14.6757 1.73715L13.3243 0.262846L1.32428 11.2628L2.67572 12.7372Z"
              fill="#17172D"
            />
            <path
              d="M2 1H14V12"
              stroke="#17172D"
              stroke-width="2"
              stroke-linecap="square"
              stroke-linejoin="round"
            />
          </svg>
        </span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.mob {
  display: none;
}

.main__hits {
  margin-top: 150px;
  margin-bottom: 150px;

  &-card-list {
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 20px;
    margin-top: 30px;
    &-p {
      color: #17172d;
      font-family: "Myriad Pro";
      font-size: 24px;
      font-style: normal;
      font-weight: 400;
      line-height: 100%; /* 24px */
    }
    &-item {
      max-width: 455px;
      min-height: 455px;
      background: #f7f7f7;
      position: relative;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      padding: 20px;
      width: 100%;
      height: 100%;

      &-title {
        color: #808080;

        font-family: "Myriad Pro";
        font-size: 20px;
        font-style: normal;
        font-weight: 400;
        line-height: 100%;
      }

      &-bordered {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        height: 100%;
        border: 1px solid #17172d;
        cursor: pointer;
        & span {
          display: flex;
          gap: 10px;
          align-items: center;
          color: #17172d;
          font-family: "Myriad Pro";
          font-size: 20px;
          font-style: normal;
          font-weight: 600;
          line-height: 90%; /* 18px */
          text-transform: uppercase;
        }
      }
      &-img {
        position: absolute;
        display: flex;
        justify-content: center;
        align-items: center;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        & img {
          width: 100%;
          height: 100%;
          user-select: none;
          object-fit: contain;
        }
      }
    }
  }
  &-head {
    display: flex;
    justify-content: space-between;
    &-name {
      color: var(---, #17172d);

      font-family: "Century Gothic";
      font-size: 16px;
      font-style: normal;
      font-weight: 700;
      line-height: 90%;
      text-transform: uppercase;
    }
    &-title {
      color: var(---, #17172d);
      position: relative;

      font-family: "Century Gothic";
      font-size: 70px;
      font-style: normal;
      font-weight: 700;
      line-height: 90%;
      letter-spacing: -1.4px;
      text-transform: uppercase;
      &::after {
        content: "";
        position: absolute;
        width: 144px;
        height: 9px;
        background: #17172d;
        bottom: 4px;
        right: 140px;
      }
      & span {
        color: #3064c7;
        font-family: "Century Gothic";
        font-size: 70px;
        font-style: normal;
        font-weight: 700;
        line-height: 90%;
        letter-spacing: -1.4px;
        text-transform: uppercase;
      }
    }
  }
}
@media screen and (max-width: 1439.99px) {
  .main__hits-card-list {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 20px;
    margin-top: 30px;
  }
  .main__hits-card-list-item {
    max-width: 100%;
    min-height: 455px;
    background: #f7f7f7;
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding: 20px;
    width: 100%;
    height: 100%;
  }
  .main__hits-head {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 20px;
  }
  .main__hits-head-title::after {
    content: "";
    position: absolute;
    width: 136px;
    height: 9px;
    background: #17172d;
    bottom: 5px;
    right: 145px;
  }
}

@media screen and (max-width: 1199.99px) {
  .main__hits-card-list {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 20px;
    margin-top: 30px;
  }
  .main__hits {
    margin-top: 35px;
    margin-bottom: 150px;
  }

  .main__hits-head-title {
    font-size: 56px !important;
    & span {
      font-size: 56px;
    }
  }

  .main__hits-head-title::after {
    content: "";
    position: absolute;
    width: 112px;
    height: 8px;
    background: #17172d;
    bottom: 4px;
    right: 114px;
  }
  .main__hits-card-list-item-img img {
    height: 75%;
  }
}

@media screen and (max-width: 991.99px) {
  .main__hits-card-list-item {
    min-height: 418px;
  }
  .main__hits-card-list-item-title {
    font-size: 18px;
  }
  .main__hits-card-list-item {
    min-height: 320px;
  }
}

@media screen and (max-width: 767.99px) {
  .mob {
    display: block !important;
  }
  .main__hits-head-title {
    display: none;
  }
  .main__hits-head-title::after {
    display: none;
  }
}

@media screen and (max-width: 539.99px) {
  .main__hits-card-list {
    grid-template-columns: repeat(1, minmax(0, 1fr));
  }
  .main__hits-card-list-item-bordered {
    padding: 20px;
  }
  .main__hits-card-list-item {
    &:nth-child(4),
    &:nth-child(6),
    &:nth-child(5) {
      display: none;
    }
  }
  .main__hits-card-list-p {
    order: -1;
  }
  .main__hits-head-title {
    font-size: 35px !important;
    & span {
      font-size: 35px;
    }
  }
  .main__hits-head-title::after {
    display: none;
  }
  .main__hits-card-list-p {
    font-size: 20px;
  }
}

@media screen and (max-width: 424.99px) {
  .main__hits-head-name {
    color: #17172d;
    font-family: "Century Gothic";
    font-size: 10px;
    font-style: normal;
    font-weight: 700;
    line-height: 90%;
    text-transform: uppercase;
  }
  .main__hits {
    margin-top: 60px;
  }
  .main__hits-head-title {
    color: #17172d;
    font-family: "Century Gothic";
    font-size: 35px;
    font-style: normal;
    font-weight: 700;
    line-height: 100%;
    letter-spacing: -0.7px;
    text-transform: uppercase;
    & span {
      color: #17172d;
      font-family: "Century Gothic";
      font-size: 35px;
      font-style: normal;
      font-weight: 700;
      line-height: 100%;
      letter-spacing: -0.7px;
      text-transform: uppercase;
    }
  }
  .main__hits-head {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 10px;
  }
  .main__hits-card-list {
    margin-top: 11px;
  }
  .main__hits-card-list-item-title {
    color: #808080;
    font-family: "Myriad Pro";
    font-size: 14px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
  }
  .main__hits-card-list-item {
    min-height: 354px;
  }
  .main__hits-card-list {
    gap: 10px;
  }
  .main__hits {
    margin-bottom: 48px;
  }
}

.main__hits-card-list-item-bottom {
  display: flex;
  justify-content: space-between;
}

@media screen and (max-width: 375.99px) {
}

@media screen and (max-width: 319.99px) {
}
</style>
