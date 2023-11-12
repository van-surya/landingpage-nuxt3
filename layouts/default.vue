<template>
  <div>
    <nav>
      <ul>
        <li>
          <nuxt-link to="/">
            <i class="fa-solid fa-house"></i>
            <span>Home</span>
          </nuxt-link>
        </li>
        <li>
          <nuxt-link to="/about">
            <i class="fa-regular fa-user"></i>
            <span>About</span>
          </nuxt-link>
        </li>
        <li>
          <nuxt-link to="/portfolio">
            <i class="fa-regular fa-images"></i>
            <span>Portfolio</span>
          </nuxt-link>
        </li>
      </ul>
    </nav>
    <div class="light">
      <button class="btn btn-light" @click="toggleColorMode">
        <i :class="iconClass"></i>
      </button>
    </div>
    <slot />
  </div>
</template> 


<script setup lang="ts">
const colorMode = useColorMode();

const toggleColorMode = () => {
  colorMode.preference = colorMode.preference === "dark" ? "light" : "dark";
};

const iconClass = ref("");

// Mengatur kelas ikon berdasarkan mode warna saat komponen dimuat
onMounted(() => {
  setIconClass();
});

// Mengatur kelas ikon setiap kali mode warna berubah
watch(
  () => colorMode.preference,
  () => {
    setIconClass();
  }
);

// Fungsi untuk mengatur kelas ikon berdasarkan mode warna
const setIconClass = () => {
  iconClass.value =
    colorMode.preference === "dark"
      ? "fa-regular fa-lightbulb"
      : "fa-solid fa-lightbulb";
};
</script>