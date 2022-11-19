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
  font-weight: 500;
  font-size: 2.0rem;
  top: 2vw;
  right: 3vw;
  position: fixed;
}

h3 {
  font-size: 1.2rem;
  position: fixed;
  bottom: 1vw;
  left: 1vw;
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
