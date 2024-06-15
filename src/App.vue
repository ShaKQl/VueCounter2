<template>
  <main>
    <div>
      <h4>The current count is...</h4>
      <h1>{{ count }}</h1>

      <button @click="addCount()">+</button>
      <button @click="subtractCount">-</button>
    </div>
  </main>
</template>

<script setup>
  import { ref } from "vue";
  let count = ref(0) 

  const addCount = ()=> {
    count.value += 1
  }
  const subtractCount = ()=> {
    count.value -= 1
  }
</script>

<style scoped>
  main{
    background: aliceblue;
    width: 100vw;
    height: 100vh; 
    display: flex;
    align-items: center;
    justify-content: center;
  }

  div{
    text-align: center;
  }
</style>