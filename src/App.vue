<script>

import TheHeader from "./components/TheHeader.vue";
import TheFooter from "./components/TheFooter.vue";
import Banner from "./components/Banner.vue";
import DcComics from "./db/dc-comics";
import Card from "./components/Card.vue"

export default {
  components: {
    TheHeader,
    TheFooter,
    Banner,
    Card,
  },

  data() {
    return {
      DcComics,
    }
  }
}
</script>

<template>
  <TheHeader></TheHeader>
  <main>
    <div class="jumbotron-img">
      <img src="./assets/img/jumbotron.jpg" alt="">
    </div>

    <div class="content-wrapper">
      <div class="container">
        <h3 class="content-sct-title">CURRENT SERIES</h3>
        <div class="row row-cols-6">
          <div class="col" v-for="card in DcComics">
            <Card 
            :img-src="card.thumb"
            :title="card.series"></Card>
          </div>
        </div>
        <div class="load-content-btn text-center">
          <span>LOAD MORE</span></div>
      </div>
    </div>
    <Banner></Banner>
  </main>
  <TheFooter></TheFooter>
</template>

<style lang="scss">
.jumbotron-img img {
  height: 360px;
  width: 100%;
  object-fit: cover;
  object-position: top;
}

.content-wrapper {
  padding-bottom: 30px;
  background-color: #1C1C1C;

  h3 {
    color: white;
  }

  .content-sct-title {
    background-color: #0282F9;
    padding: 8px 20px;
    margin-top: -30px;
    margin-bottom: 30px;
    display: inline-block;
  }

  .load-content-btn span{
    display: inline-block;
    background-color: #0282F9;
    padding: 10px 50px;
    font-weight: 600;
    color: white;

  }
}
</style>
