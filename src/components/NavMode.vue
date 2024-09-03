<template>
  <main class=" w-4/6 p-0 mx-auto mb-4 flex justify-between items-center gap-4 px-24">
    <div class="w-fit" >
        <div class="flex gap-2 justify-start items-center rounded-xl py-3 px-3 w-44 h-14  cursor-pointer">
            <img src="../assets/js.svg" alt="" class="w-10 h-10 rounded-xl" >
            <h1 class="text-xl dark:text-white">Javascript</h1>
        </div>
    </div>
    <div class=" flex justify-evenly items-center gap-1 w-fit">
        <svg width="24px" height="24px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">

<g id="SVGRepo_bgCarrier" stroke-width="0"/>

<g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"/>

<g id="SVGRepo_iconCarrier"> <circle cx="12" cy="12" r="6" :fill="lightFill"  :stroke="color" stroke-width="1.5"/> <path d="M12 2V3" :stroke="color" stroke-width="1.5" stroke-linecap="round"/> <path d="M12 21V22" :stroke="color" stroke-width="1.5" stroke-linecap="round"/> <path d="M22 12L21 12" :stroke="color" stroke-width="1.5" stroke-linecap="round"/> <path d="M3 12L2 12" :stroke="color" stroke-width="1.5" stroke-linecap="round"/> <path d="M19.0708 4.92969L18.678 5.32252" :stroke="color" stroke-width="1.5" stroke-linecap="round"/> <path d="M5.32178 18.6777L4.92894 19.0706" :stroke="color" stroke-width="1.5" stroke-linecap="round"/> <path d="M19.0708 19.0703L18.678 18.6775" :stroke="color" stroke-width="1.5" stroke-linecap="round"/> <path d="M5.32178 5.32227L4.92894 4.92943" :stroke="color" stroke-width="1.5" stroke-linecap="round"/> </g>

</svg>
    <div class="w-12 h-6 rounded-full bg-slate-400 dark:bg-violet-800 flex justify-start items-center p-1 cursor-pointer " @click="toggle();$emit('theme',mode)">
     <div class="w-5 h-5 rounded-full bg-white theme">
     </div>
    </div>
    <svg width="24px" height="24px" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" :stroke="color">

<g id="SVGRepo_bgCarrier" stroke-width="0"/>

<g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"/>

<g id="SVGRepo_iconCarrier"> <path d="M3 17C10.952 18.6176 16.6829 8.75775 11 3C16.0007 3.13144 20 7.11149 20 12C20 16.9715 16.1188 21 11 21C7.77111 21 4.65938 19.4319 3 17Z" :stroke="color" :fill="darkFill" stroke-width="1.5" stroke-linejoin="round"/> </g>

</svg>
</div>
  </main>
</template>

<script>
import gsap from 'gsap';
    export default {
        name:"NavModeComp",
        data() {
            return {
                mode:"light",
                color:"black",
                lightFill:"black",
                darkFill:"none",
            }
        },
        methods: {
            toggle() {
                if(this.mode=="light"){
                    this.mode = "dark",
                    this.color = "white"
                    this.lightFill = "none",
                    this.darkFill = "white"
               return gsap.to(".theme",{
                x:21,
                backgroundColor:"#172554",
                duration:.5
              })  
                }else{
                     this.mode = "light",
                     this.color = "black",
                     this.lightFill = "black",
                    this.darkFill = "none"
                    return gsap.to(".theme",{
                x:0,
                backgroundColor:"white",
                duration:.5
              })
                }
            
            }
        },
        emits:["theme"]
    }
</script>

<style  scoped>
@tailwind base;
@tailwind components;
@tailwind utilities;
</style>