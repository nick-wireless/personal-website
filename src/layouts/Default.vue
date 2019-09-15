<template>
  <div class="max-w-3xl mx-auto px-6 md:px-8">
    <header class="text-cp1-800 pt-10">
      <div class="flex justify-between items-center">
        <g-link class="text-lg font-semibold" to="/">Nick Hanigan</g-link>
        <div v-on:click="showSmallMenu = !showSmallMenu">
          <MenuIcon
            v-if="showSmallMenu"
            class="fill-current logo md:hidden"
          ></MenuIcon>
          <ExitIcon v-else class="logo md:hidden"></ExitIcon>
        </div>
      </div>
      <nav v-if="!showSmallMenu" class="md:hidden">
        <g-link class="pt-8 block text-base font-medium" to="/">About</g-link>
        <g-link class="pt-4 block text-base font-medium" to="/hopscotch"
          >Hopscotch</g-link
        >
        <g-link class="py-4 block text-base font-medium" to="/images"
          >Images</g-link
        >
      </nav>
      <nav
        class="hidden md:py-6 md:block md:w-full md:flex md:justify-start md:text-base md:border-b-2 md:font-semibold"
      >
        <g-link class="pl-2 pr-6" to="/">About</g-link>
        <g-link class="px-6" to="/hopscotch">Hopscotch</g-link>
        <g-link class="px-6" to="/images">Images</g-link>
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
import ExitIcon from "~/assets/svgs/icon-close-square.svg";
export default {
  name: "Default Layout",
  components: {
    MenuIcon,
    ExitIcon
  },
  data() {
    return {
      showSmallMenu: true
    };
  },
  methods: {
    toggleMenu: function() {
      return !showSmallMenu;
    }
  }
};
</script>

<style>
body {
  @apply font-sans antialiased bg-gray-100 text-base text-cp1-900;
}
.active {
  @apply text-cp1-1000 font-semibold;
}
.logo {
  width: 24px;
  height: 24px;
  /* margin-right: 10px; */
}
.primary {
  fill: theme(colors.cp1.300);
}

.secondary {
  fill: theme(colors.cp1.1000);
}
</style>
