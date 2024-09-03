<template>
  <div :class="theme">
  <main class="bg-slate-50 dark:bg-violet-950 flex flex-col justify-center items-center wrapper ">
<NavModeComp @theme="toggleTheme" />
  <div class="max-w-screen-2xl h-auto flex justify-center items-center font-mono overflow-hidden container mt-16">
<HomeComp @quiz="selectedQuiz" v-if="homePage"/>
<QuizComp v-if="quizPage"/>
</div>
</main>
</div>
</template>

<script>
import HomeComp from "./components/Home.vue"
import NavModeComp from "./components/NavMode.vue"
import QuizComp from "./components/Quiz.vue"

  export default {
    name:"App",
    components:{
      HomeComp,
      NavModeComp,
      QuizComp
    },
    data() {
      return {
        theme: "",
        homePage:true,
        quizPage:false
      }
    },
    methods: {
      toggleTheme(data) {
        this.theme = data;
      },
      selectedQuiz(){
      this.homePage = false;
      this.quizPage = true;
      }
    },

}

</script>

<style scoped>
@tailwind base;
@tailwind components;
@tailwind utilities;

*{
  font-family: "Roboto", sans-serif;
  font-weight: 400;
  font-style: normal;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.wrapper{
  height: 97vh;
}
</style>