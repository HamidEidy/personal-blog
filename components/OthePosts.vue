<template>
  <ClientOnly>
    <div class="row layoutPadding">
      <div
        class="col-lg-4 col-md-6 col-sm-12 mb-3 mb-sm-0"
        v-for="item in content"
        :key="item.id"
      >
        <div class="mb-3">
          <div class="row">
            <div class="col-8">
              <div class="text-start">
                <nuxtLink
                  :to="`/${item.id}`"
                  style="font-size: 16px; font-weight: bold"
                  >{{ item.title }}</nuxtLink
                >
                <p class="text-body-secondary">1402/09/26</p>
              </div>
            </div>
            <div class="col-4">
              <img
                src="../55.avif"
                class="img-fluid shadow-2-strong"
                alt="..."
                style="width: 100%"
              />
            </div>
          </div>
        </div>

        <hr />
      </div>
    </div>
  </ClientOnly>
</template>

<script setup>
import content from "../data/popularPosts.json";
</script>
<style scoped>
a {
  text-decoration: none;
  color: rgb(45, 45, 45);
}
</style>