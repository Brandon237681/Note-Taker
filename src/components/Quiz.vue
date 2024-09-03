<template>
    <main class="flex gap-8 w-4/6 p-4 dark:text-white justify-evenly flex-wrap">
       
    <div>
        <p class="mb-4 italic dark:text-gray-300">Question 1 of 10.</p>
        <h1 class="welcome">Do you know what <br/> the result  of this code will be ? </h1>
        <h1 class="quiz mt-4">Console.log ( <span class="text-green-500">typeOf </span> <span class="text-red-500">typeOf 1</span> ) ;</h1>
    </div>
    <div class="flex flex-col gap-5">
   <CardComp>
   <div class="w-10 h-10 rounded-md bg-slate-300 dark:bg-violet-500 text-xl flex justify-center items-center">A</div>
    <h1 class="text-xl">Chain</h1>
   </CardComp>
   <CardComp>
    <div class="w-10 h-10 rounded-md bg-slate-300 dark:bg-violet-500 text-xl flex justify-center items-center">B</div>
    <h1 class="text-xl">Number</h1>
   </CardComp>
   <CardComp>
    <div class="w-10 h-10 rounded-md bg-slate-300 dark:bg-violet-500 text-xl flex justify-center items-center">C</div>
    <h1 class="text-xl">1</h1>
   </CardComp>
   <CardComp>
    <div class="w-10 h-10 rounded-md bg-slate-300 dark:bg-violet-500 text-xl flex justify-center items-center">D</div>
    <h1 class="text-xl">True</h1>
   </CardComp>
   <button class="py-3 px-3 w-96  cursor-pointer bg-blue-500 text-white rounded-md">
     Submit answer
   </button>
    </div>
</main>
</template>

<script>
import CardComp from "../components/Card.vue"
    export default {
        name:"QuizComp",
        components:{
            CardComp,
        }
    }
</script>

<style scoped>
@tailwind base;
@tailwind components;
@tailwind utilities;

.welcome{
    font-size: 22px;
    font-family: "Roboto", sans-serif;
  font-weight: 300;
  font-style: normal;
}
.quiz{
    font-size: 22px;
    font-family: "Roboto", sans-serif;
  font-weight: 400;
  font-style: normal;
}
</style>