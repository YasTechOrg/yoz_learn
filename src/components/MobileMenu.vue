<script setup lang="ts">
defineProps<{
  showMenu: boolean
}>()
</script>

<template>
  <div class="mobileMenu d-flex flex-column" :class="{ showMenu: showMenu }">
    <img src="../assets/img/mobile_right_arrow.png" alt="back" @click="$emit('closeMenu')">

    <div class="navigation d-flex flex-column align-items-end justify-content-start">
      <a href="#">خانه</a>
      <a href="#">دوره ها</a>
      <a href="#">تماس با ما</a>
    </div>
  </div>
</template>

<style lang="sass">
@import ../assets/css/colors

.mobileMenu:not(.showMenu)
  z-index: -300
  opacity: 0

.mobileMenu
  transition: 0.2s
  position: fixed
  top: 0
  left: 0
  bottom: 0
  right: 0
  overflow: auto
  background-color: white
  z-index: 99999
  padding: 20% 10% 10%

  > img[alt=back]
    $icon_size: 35px
    height: $icon_size
    width: $icon_size

  > .navigation
    margin-top: 30px

    > a
      text-decoration: none
      color: $yoz-blue1
      font-size: 30px
      padding: 10px 0
      font-weight: 600
      white-space: nowrap

</style>