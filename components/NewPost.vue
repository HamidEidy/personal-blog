<template>
  <ClientOnly>
    <div class="row layoutPadding mt-5" @click="console.log(content.id)">
      <div class="col-lg-6 col-md-12 py-3">
        <div class="text-start pe-3">
          <small class="badge bg-danger">آخرین مقاله</small>
          <h5 class="fs-2 fw-bold">{{ content[0].title }}</h5>
          <p class="card-text">{{ content[0].description }}</p>
          <nuxt-link :to="`/${content[0].id}`" class="bluebtn"
            >مطالعه کامل</nuxt-link
          >
        </div>
      </div>

      <div class="col-lg-6 col-md-12">
        <img
          src="../assets/images/55.avif"
          style="height: 220px; width: 100%"
          class="img-fluid shadow-3-strong shadow-lg"
          alt="..."
        />
      </div>
    </div>
  </ClientOnly>
</template>

<script setup>
import content from "../data/popularPosts.json";
let data = JSON.stringify(content);
</script>

<style scoped>
</style>