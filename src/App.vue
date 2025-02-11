<script setup lang="ts">
import { ref } from 'vue'

const screenWidth = ref(window.innerWidth);
const screenHeight = ref(window.innerHeight)

console.log(screenHeight.value)
console.log(screenWidth.value)
</script>

<template>
  <div id="root">
    <header className="w-full bg-blue-400 h-[17.5vh]">
      <div className="relative top-[2.8vh] left-[3vw] bg-blue-500 w-[24.5vw] h-[22.8vh] flex text-end items-center z-10 rounded">
        <span className="place-self-center">YOUR IMAGE COLLECTION</span>
      </div>
      <img
          className="absolute top-[5.2vh] left-[30.4vw] w-[13.75vw] rounded-2xl"
          alt="logo"
          src="./assets/gul.jpg"
      />
      <div className="bg-blue-600 absolute top-[7vh] right-[3vw] h-[14.5%] w-[50%] flex items-center rounded-2xl">
        <form className="bg-blue-700 flex w-full h-[70%]">
          <input type="search" className="bg-blue-800 w-full h-full flex-1 text-white rounded-l-2xl"/>
          <button className="h-full w-[19%] flex items-center justify-center text-white bg-blue-900 rounded-r-2xl">
            FIND
          </button>
        </form>
      </div>
    </header>
    <main className="relative w-full h-[calc(100vh-17.5vh)]">
      <img alt="logo" src="./assets/ptica.jpg" className="relative w-[35%] h-[62%] left-[1%] top-[8%]">
      <div className="absolute bottom-[3%] left-[1.5%] w-[36%] h-[24%] bg-purple-300 flex items-center justify-evenly">
        <button className="bg-purple-400 text-white text-[200%]"
                @click="changePage"
                v-for="page of pages"
                type="button"
        >
          {{ page.id }}
        </button>
      </div>
    </main>
  </div>
</template>

<style scoped>

</style>
