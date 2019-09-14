<template>
  <div class="max-w-3xl mx-auto px-6 md:px-8">
    <header class="text-cp1-800 pt-10">
      <div class="flex justify-between items-center">
        <g-link class="text-lg font-semibold" to="/">Nick Hanigan</g-link>
        <MenuIcon class="fill-current logo md:hidden"></MenuIcon>
      </div>
      <nav
        class="hidden md:py-6 md:block md:w-full md:flex md:justify-start md:text-base md:border-b-2 md:font-semibold"
      >
        <g-link class="pl-2 pr-6" to="/">About</g-link>
        <g-link class="px-6" to="/hopscotch">Hopscotch</g-link>
        <g-link class="px-6" to="/blog">Images</g-link>
      </nav>
    </header>
    <slot />
  </div>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>

<script>
import MenuIcon from "~/assets/svgs/iconMenu.svg";
export default {
  name: "Default Layout",
  components: {
    MenuIcon
  }
};
</script>

<style>
body {
  @apply font-sans antialiased bg-teal-100 text-cp1-900;
}
.active {
  @apply text-cp1-1000;
}
.logo {
  width: 24px;
  height: 24px;
  /* margin-right: 10px; */
}
</style>
