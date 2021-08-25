<template>
  <nav class="navbar navbar-expand-lg navbar-dark fixed-top" id="mainNav">
    <div class="x y" style="max-width:1200px">
      <nuxt-link to="/"  class="navbar-brand" style="color: #fff;font-weight:600;font-size:24px;font-family:'Garamond', 'Georgia', 'Times New Roman', serif">
        {{ logo }}
      </nuxt-link>
      <button class="navbar-toggler" type="button" @click="show=!show" data-bs-toggle="collapse" data-bs-target="#navbarResponsive" aria-controls="navbarResponsive" aria-expanded="false" aria-label="Toggle navigation">
        Menu
      </button>
      <div class="collapse navbar-collapse mla" id="navbarResponsive">
        <ul class="navbar-nav text-uppercase ms-auto py-4 py-lg-0" >
          <li class="nav-item block font-medium py-1 md:py-2">
            <nuxt-link to="/" class="nav-link">Home</nuxt-link>
          </li>
          <li class="nav-item block font-medium py-1 md:py-2">
            <nuxt-link to="/blog" class="nav-link">Events</nuxt-link>
          </li>
          <li 
              v-for="(page, index) in pages"
              :key="index"
              class="nav-item block font-medium py-1 md:py-2">
              <nuxt-link :to="`/${page.slug}`" class="nav-link">{{ page.title }}</nuxt-link></li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script lang="ts">
import { Component, Vue } from 'nuxt-property-decorator';
import settings from '@/content/settings/general.json';

@Component
export default class Header extends Vue {
  get pages(): Page[] {
    return this.$store.state.pages;
  }

  logo = settings.logo;
}
</script>

<style lang="scss">
.nav {
  ul li > a {
    &.nuxt-link-active {
      @apply font-bold;
    }
  }
}


@media (max-width: 767.98px) {
.shownav{display:block !important}
}

</style>
