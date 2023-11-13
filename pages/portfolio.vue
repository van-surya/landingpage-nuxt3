<template>
  <div>
    <div class="portfolio">
      <div class="container">
        <h1>Our <span>Portfolio</span></h1>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Nam sint
          nesciunt minus iste a
        </p>
        <div class="row">
          <div
            v-for="(item, index) in items.slice(0, 6)"
            :key="index"
            class="col-lg-4 mt-3"
          >
            <div class="card">
              <img :src="item.imageUrl" :alt="item.imageUrl" />
              <div class="card-body">
                <div class="text">
                  <h5>{{ item.title }}</h5>
                  <div class="social">
                    <a v-if="!item.codepen" :href="item.youtube" class="me-2">
                      <i class="fa-brands fa-youtube"></i>
                      <span>More Link</span>
                    </a>
                    <a v-if="item.codepen" :href="item.codepen">
                      <i class="fa-brands fa-codepen"></i>
                      <span>More Link</span>
                    </a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>

        <ul class="pagination_">
          <li class="page_item active" aria-current="page">
            <a class="page-link" href="#">1</a>
          </li>
          <li class="page_item">
            <a class="page-link" href="#">2</a>
          </li>
          <li class="page_item">
            <a class="page-link" href="#">3</a>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>


<script setup lang="ts">
useSeoMeta({
  title: "Welcome - Surya Van",
  ogTitle: 'My Amazing Site',
  description: 'This is my amazing site, let me tell you all about it.',
  ogDescription: 'This is my amazing site, let me tell you all about it.',
  ogImage: 'https://example.com/image.png',
  twitterCard: 'summary_large_image',
});

const items = [
  {
    imageUrl:
      "https://cdn.dribbble.com/users/9979443/screenshots/17026249/media/aeaee0636e4d56836f9998833f701994.jpg?resize=400x300&vertical=center",
    title: "Title Desc loream",
    codepen: "/codepen",
  },
  {
    imageUrl:
      "https://cdn.dribbble.com/users/9979443/screenshots/17245036/media/73db05760805b027906a509f550f1017.jpg?resize=400x300&vertical=center",
    title: "Title Desc loream",
    youtube: "/youtube",
  },
  {
    imageUrl:
      "https://cdn.dribbble.com/users/9979443/screenshots/17358764/media/e10a43258356cb33949fcb159c8ced13.jpg?resize=400x300&vertical=center",
    title: "Title Desc loream",
    codepen: "/codepen",
  },
  {
    imageUrl:
      "https://cdn.dribbble.com/users/9979443/screenshots/17077622/media/a23310b1005e847a30a17495d7066808.jpg?resize=400x300&vertical=center",
    title: "Title Desc loream",
    youtube: "/youtube",
  },
  {
    imageUrl:
      "https://cdn.dribbble.com/users/9979443/screenshots/17067783/media/a4812e58c67752d9a65913c2bdf8544c.jpg?resize=400x300&vertical=center",
    title: "Title Desc loream",
    codepen: "/codepen",
  },
  {
    imageUrl:
      "https://cdn.dribbble.com/users/9979443/screenshots/17057878/media/f3cd875343f3189449f467c620aebfaf.jpg?resize=400x300&vertical=center",
    title: "Title Desc loream",
    codepen: "/codepen",
  },
];
</script>
 