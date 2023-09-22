<script setup>
  import SideBar from "./components/SideBar.vue";
  import ImageGallery from "./components/ImageGallery.vue"
  import {ref} from "vue"

  const isWithColor = ref(true)

  const onSelectionOption = (isColor) => {
    isWithColor.value = isColor;
  } 
</script>

<template>
  <v-app>
    <!--- SideBAr Components --->
  <SideBar @selectOption="onSelectionOption"/>
    <v-main>
      <!--Cards-->
      <ImageGallery   :isWithColor="isWithColor" />
    </v-main>
  </v-app>
</template>

<script>

</script>
