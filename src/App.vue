<template>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <link
    rel="icon"
    type="image/png"
    sizes="32x32"
    href="./images/favicon-32x32.png"
  />

  <title>Frontend Mentor | Advice generator app</title>

  <div class="tudo">
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
};
</script>

<style lang="scss">

body{
  background-color: hsl(218, 23%, 16%);
}
</style>
