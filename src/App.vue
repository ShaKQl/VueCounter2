<template>
  <main>
    <div class="display">
      <div class="display__case--zero">
        <h4>The current count is...</h4>
        <h1>{{ count }}</h1>
      </div>

      <div class="display__case--positive">
        <h4>The current count is {{ count }}</h4>
      </div>

      <div class="button__wrapper">
        <button class="button" @click="addCount(), checkForCount">+</button>
        <button class="button" @click="subtractCount(), checkForCount">-</button>
      </div>
    </div>
  </main>
</template>







<script setup>
  import { ref } from "vue";
  let count = ref(0)

  const addCount = () => {
    count.value += 1
  }
  const subtractCount = () => {
    if (count.value == 0) {
      return count.value
    }
    else {
      count.value -= 1
    }
  }
</script>







<style scoped>
main {
  background: aliceblue;
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

div {
  text-align: center;
}

.button {
  width: 150px;
  width: 100%;
  border-radius: 25px;
  background-color: #858585;
  border: none;
  transition: 0.5s ease-in-out;
}

.button__wrapper {
  display: flex;
  gap: 15px;
  margin-top: 15px;
}

.button:hover {
  background-color: #393939;
  color: #fff;
}

.display__case--positive{
  display: none;
}
</style>