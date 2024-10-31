<script setup lang="ts">
const route = useRoute()
</script>



<template>
  <section class="contact container">
    <h2 class="title">
      Контакты
    </h2>

    <div class="contact_block">
      
      <div class="first_block">

        <div class="connect">
          <svg width="10" height="10" viewBox="0 0 10 10" fill="none" xmlns="http://www.w3.org/2000/svg">
            <rect width="10" height="10" fill="#17172D"/>
          </svg>

          <button class="connect-button">
            Свяжитесь с нами
          </button>

        </div>

          <p class="dscr">
            Свяжитесь с нами и мы ответим на вопросы
          </p>
        <div>

          <div class="connect-details">
            <div class="address">
              <h3 class="address_title">/Адрес</h3>
              <p class="address_sub_title">г. Санкт-Петербург<br>ул. Латышских Стрелков, д. 27, литера А, пом. 5-Н</p>
            </div>

            <div class="working-hours">
                <h3 class="wh_title">/Режим работы</h3>
                <p class="wh_sub_title">Пн. – Чт.: с 9:00 до 18:00<br>Пт.: с 9:00 до 17:00</p>
              </div>
           </div>

           <div class="connect-phone-email">
              <p class="phone">+7 812 309-86-00</p>
              <p class="email">E-MAIL: INFO@PHC.SU></p>
            </div>

        </div>


      </div>





    </div>




  </section>
</template>

<!-- <script>
export default {
  data() {
    return {
      showContactInfo: false, 
      showForm: false,
      form: {
        company: '',
        phone: '',
        name: '',
        email: '',
        request: '',
        file: null,
        agree: false,
      },
    };
  },
  methods: {
    handleFileUpload(event) {
      this.form.file = event.target.files[0];
    },
    submitForm() {
      if (this.form.agree) {
        alert("Форма успешно отправлена!");
        // Логика отправки данных формы
      } else {
        alert("Пожалуйста, согласитесь с политикой конфиденциальности.");
      }
    },
  },
};
</script> -->


<style lang="scss" scoped> 



</style>