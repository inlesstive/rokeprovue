<template>
  <div class="profile__section">
    <div class="details" v-if="false">
      <ul class="details__list">
        <li class="details__list-item">
          <span class="details__message">Реквизиты не добавлены</span>
        </li>
        <li class="details__list-item">
          <p class="details__description">
            У вас пока нет сохраненных реквизитов. Добавьте <br />
            данные — это ускорит оформление заказа.
          </p>
        </li>
        <li class="details__list-item">
          <button class="details__popup-button" @click="isOpen = !isOpen">
            <span> Добавить новые реквизиты </span>
          </button>
        </li>
      </ul>
    </div>

    <div class="details__cards">
      <div class="details__card" v-for="_ in 3">
        <span class="details__card-title">
          Roke
          <div class="details__card-buttons">
            <button
              class="details__card-button details__card-button--edit"
              @click="isOpen = !isOpen"
            >
              <svg
                width="28"
                height="27"
                viewBox="0 0 28 27"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M24.6278 3.69818C24.9573 3.36868 24.9573 2.83444 24.6278 2.50494C24.2983 2.17544 23.7641 2.17544 23.4346 2.50494L12.1847 13.755L11.6562 15.4766L13.3778 14.9481L24.6278 3.69818ZM7.15625 3.38281C5.13695 3.38281 3.5 5.01977 3.5 7.03906V19.9766C3.5 21.9958 5.13695 23.6328 7.15625 23.6328H20.0938C22.113 23.6328 23.75 21.9958 23.75 19.9766V10.9766C23.75 10.5106 23.3722 10.1328 22.9062 10.1328C22.4403 10.1328 22.0625 10.5106 22.0625 10.9766V19.9766C22.0625 21.0639 21.1811 21.9453 20.0938 21.9453H7.15625C6.06894 21.9453 5.1875 21.0639 5.1875 19.9766V7.03906C5.1875 5.95175 6.06894 5.07031 7.15625 5.07031H16.1562C16.6222 5.07031 17 4.69255 17 4.22656C17 3.76057 16.6222 3.38281 16.1562 3.38281H7.15625Z"
                  fill="#17172D"
                />
              </svg>
            </button>
            <button class="details__card-button details__card-button--delete">
              <svg
                width="27"
                height="27"
                viewBox="0 0 27 27"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M11.252 5.625H15.752C15.752 4.38236 14.7446 3.375 13.502 3.375C12.2593 3.375 11.252 4.38236 11.252 5.625ZM9.56445 5.625C9.56445 3.45038 11.3273 1.6875 13.502 1.6875C15.6766 1.6875 17.4395 3.45038 17.4395 5.625H23.9082C24.3742 5.625 24.752 6.00276 24.752 6.46875C24.752 6.93474 24.3742 7.3125 23.9082 7.3125H22.4242L21.1057 20.9376C20.8965 23.1001 19.0791 24.75 16.9065 24.75H10.0974C7.92481 24.75 6.1075 23.1001 5.89822 20.9376L4.57967 7.3125H3.0957C2.62972 7.3125 2.25195 6.93474 2.25195 6.46875C2.25195 6.00276 2.62972 5.625 3.0957 5.625H9.56445ZM11.8145 10.9688C11.8145 10.5028 11.4367 10.125 10.9707 10.125C10.5047 10.125 10.127 10.5028 10.127 10.9688V19.4062C10.127 19.8722 10.5047 20.25 10.9707 20.25C11.4367 20.25 11.8145 19.8722 11.8145 19.4062V10.9688ZM16.0332 10.125C16.4992 10.125 16.877 10.5028 16.877 10.9688V19.4062C16.877 19.8722 16.4992 20.25 16.0332 20.25C15.5672 20.25 15.1895 19.8722 15.1895 19.4062V10.9688C15.1895 10.5028 15.5672 10.125 16.0332 10.125ZM7.57788 20.775C7.70344 22.0725 8.79383 23.0625 10.0974 23.0625H16.9065C18.2101 23.0625 19.3004 22.0725 19.426 20.775L20.7288 7.3125H6.27504L7.57788 20.775Z"
                  fill="#17172D"
                />
              </svg>
            </button>
          </div>
        </span>

        <div class="details__card-info">
          <span class="details__card-company"> Компания: Roke company </span>
        </div>
        <div class="details__card-info">
          <span class="details__card-inn"> ИНН: 231231321323 </span>
        </div>
      </div>
      <button class="details__popup-button" @click="isOpen = !isOpen">
        <span> Добавить новые реквизиты </span>
      </button>
    </div>

    <UiModal v-if="isOpen" @closeModal="closeModal"></UiModal>
  </div>
</template>

<script setup>
const isOpen = ref(false);

const closeModal = () => {
  isOpen.value = false;
};
</script>

<style lang="scss" scoped>
.profile__section {
  flex-basis: 85%;
}
.details {
  &__card-button--delete {
    cursor: pointer;
  }
  &__card-button--edit {
    cursor: pointer;
  }
  &__card-button {
    background-color: white;
  }
  &__popup-button {
    grid-column: 1 / -1;
  }
  &__card-buttons {
    display: flex;
    gap: 16.88px;
  }
  &__card-title {
    color: #17172d;
    font-family: "Myriad Pro";
    font-size: 40px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
    display: flex;
    justify-content: space-between;
    margin-bottom: 108px;
  }
  &__card {
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    padding: 20px;
    background-color: white;
    border: 1px solid #d9d9d9;
    max-width: 508px;
  }
  &__cards {
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    gap: 20px;
  }
  &__list {
    display: flex;
    align-items: flex-start;
    gap: 20px;
    flex-direction: column;
  }
  & {
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
  }
  &__message {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 40px;
    font-style: normal;
    font-weight: 400;
    line-height: 90%;
  }
  &__description {
    color: #000;
    font-family: "Myriad Pro";
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
  }
  &__popup-button {
    padding: 10px;
    background-color: white;
    color: #000;
    text-transform: none;
    border: 1px solid #d9d9d9;
    cursor: pointer;
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    line-height: 100%;
    font-family: "Myriad Pro";
    transition: 0.3s;
  }
  &__popup-button:hover {
    background-color: #3064c7;
    color: white;
  }
}

@media screen and (max-width: 991.99px) {
  .details__cards {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 20px;
  }
}
@media screen and (max-width: 767.99px) {
  .details__cards {
    display: grid;
    grid-template-columns: repeat(1, minmax(0, 1fr));
    gap: 20px;
  }
  .details__card[data-v-65f97821] {
    max-width: 100%;
  }
}
</style>
