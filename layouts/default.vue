<template>
  <div>
    <nav>
      <ul>
        <li>
          <nuxt-link to="/">
            <i class="fa-solid fa-house"></i>
            <span>Home</span></nuxt-link>
        </li>
        <li>
          <nuxt-link to="/about">
            <i class="fa-regular fa-user"></i> <span>About</span></nuxt-link>
        </li>
        <li>
          <nuxt-link to="/portfolio">
            <i class="fa-regular fa-images"></i>
            <span>Portfolio</span></nuxt-link>
        </li>
      </ul>
    </nav> 
    <div class="light">
      <button class="btn btn-light">
        <i class="fa-regular fa-lightbulb"></i>
      </button>
    </div>
    <slot />
  </div>
</template> 