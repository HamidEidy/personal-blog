<template>
  <ClientOnly>
    <div class="row">
      <div
        class="col-lg-4 col-md-6 col-sm-12 mb-3 mb-sm-0"
        v-for="item in data.slice(1, 4)"
        :key="item.id"
        @click="showid(item)"
      >
        <div style="height: 100%; padding-top: 50px">
          <img src="../assets/images/55.avif" class="card-img-top" alt="..." />

          <div class="text-start">
            <div class="d-flex justify-content-between mt-3">
              <!-- <p class="text-warning">{{ item.category }}</p> -->
              <p class="text-body-secondary d-inline">{{ item.date }}</p>
              <nuxt-link :to="`/${item.id}`"
                ><h1>{{ item.title }}</h1></nuxt-link
              >
            </div>

            <p class="card-text">
              {{ item.description }}
            </p>
          </div>
          <nuxt-link :to="`/${item.id}`">
            <i class="bi bi-arrows-fullscreen"></i>
          </nuxt-link>
        </div>
        <hr />
      </div>
    </div>
  </ClientOnly>
</template>

<script setup>
import data from "../data/popularPosts.json";
</script>

<style scoped>
h1 {
  font-size: 20px;
  color: rgb(31, 31, 31);
  text-decoration: none !important;
  display: inline;
}
a {
  text-decoration: none;
  display: inline;
}
</style>