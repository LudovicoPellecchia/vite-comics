<script>

import TheHeader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";
import Banner from "./components/Banner.vue";

export default {
  components: {
    TheHeader,
    TheFooter,
    Banner,
  }
}
</script>

<template>
  <TheHeader></TheHeader>
  <main>
    <div class="content-wrapper">
      <div class="container">
        <h3> -> Content goes here &lt- </h3>
      </div>
    </div>
    <Banner></Banner>


  </main>
</template>

<style lang="scss">
.content-wrapper {
  background-color: #1C1C1C;
  padding: 3rem;

  h3 {
    color: white;
  }

}
</style>
