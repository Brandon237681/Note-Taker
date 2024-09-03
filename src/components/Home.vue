<template>
    <main class="flex gap-8 w-4/6 p-4 dark:text-white justify-evenly flex-wrap">
    <div>
        <h1 class="welcome">Welcome to the <br/> <b>Frontend Quiz !</b> </h1>
        <p class="mt-6 italic dark:text-gray-300">Pick a subject to get start.</p>
    </div>
    <div class="flex flex-col gap-5">
   <CardComp @click="$emit('quiz','html')">
    <img src="../assets/html.svg" alt="" class="w-10 h-10 rounded-md" >
    <h1 class="text-xl">HTML</h1>
   </CardComp>
   <CardComp @click="$emit('quiz','css')">
    <img src="../assets/css.svg" alt="" class="w-10 h-10 rounded-md" >
    <h1 class="text-xl">CSS</h1>
   </CardComp>
   <CardComp @click="$emit('quiz','javascript')">
    <img src="../assets/js.svg" alt="" class="w-10 h-10 rounded-xl" >
    <h1 class="text-xl">Javascript</h1>
   </CardComp>
   <CardComp @click="$emit('quiz','react js')">
    <img src="../assets/react.svg" alt="" class="w-10 h-10 rounded-md" >
    <h1 class="text-xl">React js</h1>
   </CardComp>
    </div>
</main>
</template>

<script>
import CardComp from "../components/Card.vue"
    export default {
        name:"HomeComp",
        components:{
            CardComp,
        },
    emits:["quiz"]
    }
</script>

<style scoped>
@tailwind base;
@tailwind components;
@tailwind utilities;

.welcome{
    font-size: 42px;
    font-family: "Roboto", sans-serif;
  font-weight: 100;
  font-style: normal;
}
</style>