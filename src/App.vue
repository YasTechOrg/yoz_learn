<script setup lang="ts">

// IMPORTS
import {defineAsyncComponent, ref} from "vue"
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'

// DEFINE COMPONENTS
const MobileMenu = defineAsyncComponent(() => import("./components/MobileMenu.vue"))

// VARIABLES
const isMenuShow = ref(false)
</script>

<template>
  <div id="home">

    <!-- Desktop and Mobile Header -->
    <header>
      <div class="desktop row">
        <div class="col-4 account d-flex justify-content-end align-items-center flex-row-reverse">
          <button type="button">ثبت نام</button>
          <button type="button">ورود</button>
        </div>
        <div class="col-4 navigation d-flex justify-content-center align-items-center flex-row-reverse">
          <a href="#">خانه</a>
          <a href="#">دوره ها</a>
          <a href="#">تماس با ما</a>
        </div>
        <div class="col-4 d-flex justify-content-end align-items-center">
          <img src="./assets/img/header.png" alt="Yoz Learn">
        </div>
      </div>

      <div class="mobile row m-0">
        <div class="col-6 d-flex align-items-center justify-content-start p-0">
          <img src="./assets/img/header.png" alt="Yoz Learn">
        </div>
        <div class="col-6 d-flex align-items-center justify-content-end p-0">
          <img src="./assets/img/burger.png" alt="MENU" @click="isMenuShow = !isMenuShow">
        </div>
      </div>
    </header>

    <!-- Mobile Menu -->
    <MobileMenu :showMenu="isMenuShow" @closeMenu="isMenuShow = false"/>

    <!-- Content Section 1 -->
    <section data-s-1 class="row position-relative">
      <img src="./assets/img/section1_vector2.png" class="position-absolute" alt="vector_play">
      <div class="left col-lg-6 d-flex flex-column align-items-center justify-content-center">
        <img src="./assets/img/section1_vg2.png" alt="vg2">

        <div class="ic_mobile d-none justify-content-center">
          <img src="./assets/img/section1_vg2.png" alt="vg2_mobile">
          <img src="./assets/img/section1_vector2.png" alt="vector_play_mobile">
        </div>

        <div class="c1 d-flex justify-content-center align-items-center">
          <div class="d-flex align-items-center justify-content-evenly w-100">
            <img src="./assets/img/section1_brand1.png" alt="Google">
            <img src="./assets/img/section1_brand2.png" alt="Coursera">
            <img src="./assets/img/section1_brand3.png" alt="Hubspot">
          </div>
        </div>
      </div>

      <div class="right col-lg-6 d-flex flex-column align-items-end justify-content-end">
        <div class="d-flex justify-content-end">
          <div class="d-flex flex-column justify-content-center align-items-end">
            <h1 class="main_title text-end" dir="rtl">اینجا زبان علم فارسیه!</h1>
            <p class="main_description">ما براتون کار بردی ترین آموزش های بین المللی با  مدرک معتبر از بهترین دانشکاه ها، شرکت ها و پلتفرم های آموزشی مانند COURSERA</p>
          </div>
          <div class="ms-3">
            <img src="./assets/img/section1_vector1.png" alt="vector">
          </div>
        </div>

        <img src="./assets/img/section1_vg1.png" alt="vg1">
      </div>
    </section>

    <!-- Content Section 2 -->
    <section data-s-2 class="d-flex flex-column align-items-center">
<!--      <img src="./assets/img/section2_line1.png" alt="line">-->
      <div class="p1 d-flex align-items-center justify-content-center">
        <h3>دوره ها در چند دسته</h3>
        <img src="./assets/img/section2_vector1.png" alt="vector">
      </div>
      <p class="p2 text-center">
        دیجیتال مارکتینگ، دیزاین ، برنامه نویسی، تولید محتوا ، مدیریت
        <br>ترجمه ، دوبله و توسعه  داده میشود
      </p>

      <div class="p4 d-none">
        <carousel :items-to-show="1" :wrap-around="true">
          <slide class="ac d-flex flex-column justify-content-between">
            <div>
              <h5>مبانی دیجیتال مارکتینگ</h5>
              <h5>Fundamentals of digital marketing</h5>
            </div>

            <div class="d-flex flex-column align-items-center">
              <img src="./assets/img/section2_brand1_mobile.png" alt="Google">
              <button type="button">شروع کن</button>
            </div>
          </slide>

          <slide class="nac position-relative d-flex flex-column justify-content-end">
            <img src="./assets/img/section2_brand2.png" class="position-absolute" alt="coursera">
            <div class="text-center">
              در حال آماده سازی
            </div>
          </slide>

          <slide class="nac position-relative d-flex flex-column justify-content-end">
            <img src="./assets/img/section2_brand3.png" class="position-absolute" alt="coursera">
            <div class="text-center">
              در حال آماده سازی
            </div>
          </slide>

          <template #addons>
            <navigation />
            <pagination />
          </template>
        </carousel>
      </div>

      <div class="p3  d-flex justify-content-center align-items-center">
        <div class="ac d-flex flex-column justify-content-between">
          <div>
            <h5>مبانی دیجیتال مارکتینگ</h5>
            <h5>Fundamentals of digital marketing</h5>
          </div>

          <div class="d-flex flex-column align-items-start">
            <img src="./assets/img/section2_brand1.png" alt="Google">
            <button type="button">شروع کن</button>
          </div>
        </div>

        <div class="nac position-relative d-flex flex-column justify-content-end">
          <img src="./assets/img/section2_brand2.png" class="position-absolute" alt="coursera">
          <div class="text-center">
            در حال آماده سازی
          </div>
        </div>

        <div class="nac position-relative d-flex flex-column justify-content-end">
          <img src="./assets/img/section2_brand3.png" class="position-absolute" alt="coursera">
          <div class="text-center">
            در حال آماده سازی
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<style src="./assets/sass/style.sass" lang="sass"></style>
<style src="./assets/sass/carousel/carousel_home1.sass" lang="sass"></style>
<style lang="sass">
// FONTS
@font-face
  font-family: dana
  font-style: normal
  font-weight: 10
  src: url("./assets/fonts/Dana-Hairline.ttf")

@font-face
  font-family: dana
  font-style: normal
  font-weight: 100
  src: url("./assets/fonts/Dana-Thin.ttf")

@font-face
  font-family: dana
  font-style: normal
  font-weight: 200
  src: url("./assets/fonts/Dana-UltraLight.ttf")

@font-face
  font-family: dana
  font-style: normal
  font-weight: 300
  src: url("./assets/fonts/Dana-Light.ttf")

@font-face
  font-family: dana
  font-style: normal
  font-weight: 500
  src: url("./assets/fonts/Dana-Medium.ttf")

@font-face
  font-family: dana
  font-style: normal
  font-weight: 600
  src: url("./assets/fonts/Dana-DemiBold.ttf")

@font-face
  font-family: dana
  font-style: normal
  font-weight: 800
  src: url("./assets/fonts/Dana-ExtraBold.ttf")

@font-face
  font-family: dana
  font-style: normal
  font-weight: 900
  src: url("./assets/fonts/Dana-Black.ttf")

@font-face
  font-family: dana
  font-style: normal
  font-weight: 930
  src: url("./assets/fonts/Dana-ExtraBlack.ttf")

@font-face
  font-family: dana
  font-style: normal
  font-weight: 960
  src: url("./assets/fonts/Dana-Heavy.ttf")

@font-face
  font-family: dana
  font-style: normal
  font-weight: 990
  src: url("./assets/fonts/Dana-fat.ttf")

@font-face
  font-family: dana
  font-style: normal
  font-weight: bold
  src: url("./assets/fonts/Dana-ExtraBold.ttf")

@font-face
  font-family: dana
  font-style: normal
  font-weight: normal
  src: url("./assets/fonts/Dana-Regular.ttf")
</style>