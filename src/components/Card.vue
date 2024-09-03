<template>
    <div>
        <div class="flex gap-5 justify-start items-center rounded-xl py-3 px-3 w-96  cursor-pointer bg-slate-200 dark:bg-violet-900 dark:hover:bg-violet-800">
         <slot></slot>
        </div>
    
    </div>
</template>

<script>
    export default {
        name:"CardComp"
    }
</script>

<style scoped>
@tailwind base;
@tailwind components;
@tailwind utilities;
</style>