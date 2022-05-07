<script setup lang="ts">

// IMPORTS
import {defineAsyncComponent, ref} from "vue"

// DEFINE COMPONENTS
const MobileMenu = defineAsyncComponent(() => import("./components/MobileMenu.vue"))

// VARIABLES
const isMenuShow = ref(false)
</script>

<template>
  <div id="home">
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

    <MobileMenu :showMenu="isMenuShow" @closeMenu="isMenuShow = false"/>
  </div>
</template>

<style src="./assets/css/style.sass" lang="sass"></style>
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