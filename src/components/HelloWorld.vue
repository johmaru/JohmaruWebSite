<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3>
      Johmaruのウェブサイトです
      <a href="https://twitter.com/Johmaru_gamer" target="_blank" rel="noopener">Twitter</a>
    </h3>
  </div>
</template>

<style scoped>
h1 {

  font-size: 25px;
  top: 1rem;
  left: 0rem;
  position: fixed;
}

h3 {
  font-size: 1.5vmax;
  position: fixed;
  bottom: 1rem;
  left: 1rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
