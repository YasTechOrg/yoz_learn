<script setup lang="ts">
import {ref} from "vue";
import {Carousel, Slide} from 'vue3-carousel';

const courses = ref([
  {
    ready: 1,
    source: "./assets/img/pic_google_digital.svg",
    nameFa: "مبانی دیجیتال مارکتینگ",
    nameEn: "Fundamentals of digital marketing"
  },
  {ready: 0, source: "./assets/img/pic_coursera.svg", nameFa: "", nameEn: ""},
  {ready: 0, source: "./assets/img/pic_hubspot.svg", nameFa: "", nameEn: ""},
])
const settings = {
  itemsToShow: 2,
  snapAlign: 'start',
}

</script>

<template>
  <div id="home">
    <header>
      <div class="safe d-flex justify-content-between">
        <div class="account d-flex align-content-center">
          <button class="btn me-2 fw-bolder mt-auto mb-auto">
            ورود
          </button>
          <button class="btn fw-bolder mt-auto mb-auto">
            ثبت نام
          </button>
        </div>
        <div class="d-flex align-items-center justify-content-around pages">
          <a href="#">
            خانه
          </a>
          <div class="dropdown">
            <button class="btn dropdown-toggle d-flex flex-row-reverse align-items-center" type="button"
                    id="coursesDropDown" data-bs-toggle="dropdown" aria-expanded="false">
              دوره ها
            </button>
            <ul class="dropdown-menu" aria-labelledby="coursesDropDown">
              <li><a class="dropdown-item" href="#">...</a></li>
              <li><a class="dropdown-item" href="#">...</a></li>
              <li><a class="dropdown-item" href="#">...</a></li>
            </ul>
          </div>
          <a href="#">تماس با ما</a>
        </div>
        <div class="d-flex logo">
          <img src="./assets/icon/icon_logo.svg" width="50px" alt="logo">
          <p class="mt-auto mb-auto">
            <span>
              YOZ
            </span>
            <span>
              LEARN
            </span>
          </p>
        </div>
        <img src="./assets/icon/icon_hamburger_menu.svg" class="d-none menu" alt="menu">
      </div>
    </header>
    <div class="d-flex first flex-wrap">
      <div class="position-relative">
        <div>
          <img src="./assets/icon/icon_shapes1.svg" alt="shape">
          <img class="position-absolute" src="./assets/icon/icon_play.svg" alt="shape">
        </div>
        <div>
          <div class="d-flex justify-content-around">
            <img src="./assets/img/pic_google_digital.svg" alt="Google Digital Garage">
            <img src="./assets/img/pic_coursera.svg" alt="coursera">
            <img src="./assets/img/pic_hubspot.svg" alt="HubSpot">
          </div>
        </div>
      </div>
      <div class="position-relative text-end pe-3 ps-3">
        <div class="d-flex align-content-center justify-content-end">
          <p class="mt-auto mb-auto">
            اینجا زبان علم فارسیه!
          </p>
          <img src="./assets/icon/icon_shape2.svg" class="ms-2" width="31" alt="shape">
        </div>
        <p class="mt-4 mb-5">
          ما براتون کار بردی ترین آموزش های بین المللی با مدرک معتبر از بهترین دانشکاه ها، شرکت ها و پلتفرم های آموزشی
          مانند COURSERA
        </p>
        <img class="w-50" src="./assets/icon/icon_shape3.svg" alt="">
      </div>
    </div>
    <div class="second mt-5">
      some code ....
      <!--      <div class="carousel-section">
              <Carousel :autoplay="1500" :settings="settings" :wrap-around="true">
                <Slide v-for="slide in courses" :key="slide">
                   <div class="carousel__item">
                    <div v-show="slide.ready === 0">
                      &lt;!&ndash;                <img :src="require('./assets/img/'+slide.source)" alt="source">&ndash;&gt;
                      <button>
                        در حال آماده سازی
                      </button>
                    </div>
                    <div v-show="slide.ready === 1">
                      <p>
                        {{ slide.nameFa }}
                      </p>
                      <p>
                        {{ slide.nameEn }}
                      </p>
                      &lt;!&ndash;                <img :src="require('./assets/img/'+slide.source)" alt="source">&ndash;&gt;
                      <button>
                        شروع کن
                      </button>
                    </div>
                  </div>
                </Slide>
              </Carousel>
            </div>-->
    </div>
    <div class="third d-flex mt-5">
      <div class="w-50 d-flex flex-column align-items-center justify-content-center">
        <div class="yoz-card">
          <div>
            <p class="mb-0">
              با
              <span class="text-yoz-green">
              دوره مبانی دیجیتال مارکتینگ
            </span>
              ما بر اصول بازاریابی دیجیتال مسلط شوید. ۲۶ ماژول برای کاوش وجود دارد که همگی
              توسط مربیان
              <span class="text-yoz-green">
              Google
            </span>
              ایجاد شده‌اند، مملو از تمرین‌های عملی و نمونه‌های واقعی برای کمک به شما برای تبدیل دانش به عمل
            </p>
          </div>
        </div>
        <button class="btn">
          اطلاعات بیشتر و ثبت نام
        </button>
      </div>
      <div class="w-50">
        <p class="fw-bold">
          گوگل <span>مدرکتو میده</span>
        </p>
        <p class="fw-bold me-4">
          یه قدم جدی به سوی دنیای دیجیتال مارکتینگ
        </p>
        <div class="d-flex justify-content-between">
          <div class="w-100 position-relative">
            <img src="./assets/icon/icon_shape5.svg" class="shape2 position-absolute" alt="shape">
            <img src="./assets/icon/icon_shape6.svg" class="shape7 position-absolute" alt="shape">
            <img src="./assets/img/pic_google_logo.svg" class="google-logo" alt="google logo">
          </div>
          <div class="d-flex flex-column justify-content-center">
            <img src="./assets/icon/icon_shapes4.svg" class="shape1 ms-2" alt="shape">
            <div class="position-relative">
              <img src="./assets/icon/icon_shape5.svg" class="shape3 position-absolute" alt="shape">
              <img src="./assets/icon/icon_shape8.svg" class="shape4 position-absolute" alt="shape">
              <img src="./assets/icon/icon_shape7.svg" class="shape5 position-absolute" alt="shape">
              <img src="./assets/icon/icon_shape7.svg" class="shape6 position-absolute" alt="shape">
            </div>
          </div>
        </div>
        <p>
          Digital Garage
        </p>
      </div>
    </div>
  </div>
</template>

<style src="./assets/css/style.sass" lang="sass"></style>
