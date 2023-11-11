<template>
  <div class="hero">
    <div class="container">
      <div class="row">
        <div class="col-lg-6 hero_image">
          <img src="~/assets/images/hero-image.png" alt="" />
        </div>
        <div class="col-lg-6 hero_caption">
          <h1>Surya Vans</h1>
          <span>i'am Frontend Developer</span>
          <div class="hero_caption_social">
            <nuxt-link to="/">
              <i class="fa-brands fa-github"></i>
            </nuxt-link>
            <nuxt-link to="/">
              <i class="fa-brands fa-youtube"></i>
            </nuxt-link>
            <nuxt-link to="/">
              <i class="fa-brands fa-codepen"></i>
            </nuxt-link>
            <nuxt-link to="/">
              <i class="fa-brands fa-hackerrank"></i>
            </nuxt-link>
            <nuxt-link to="/">
              <i class="fa-brands fa-dribbble"></i>
            </nuxt-link>
          </div>
          <button class="btn btn_play">
            <i class="fa-regular fa-circle-play"></i>
            <span>Play</span>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>


<script setup lang="ts">
useHead({
  title: "Welcome - Surya Van",
});
</script>