<template>
  <div class="max-w-3xl mx-auto px-6 md:px-8">
    <header class="text-cp1-800 pt-10">
      <div class="flex justify-between items-center">
        <div id="profile-pic" class="flex items-center md:flex-col ">
          <div class="pr-3 md:mb-4 md:pl-4">
            <g-image
              src="~/assets/images/nickwithnacho.jpg"
              class=" w-10 h-10 rounded-full object-cover object-top shadow-lg md:w-24 md:h-24"
            ></g-image>
          </div>
          <g-link class="text-lg font-semibold" to="/">Nick Hanigan</g-link>
        </div>
        <div v-on:click="showSmallMenu = !showSmallMenu">
          <MenuIcon
            v-if="showSmallMenu"
            class="fill-current logo md:hidden"
          ></MenuIcon>
          <ExitIcon v-else class="logo md:hidden"></ExitIcon>
        </div>
      </div>
      <nav v-if="!showSmallMenu" class="md:hidden border-b-2 ">
        <g-link class="pt-4 block text-base font-medium" to="/">About</g-link>
        <g-link class="pt-4 block text-base font-medium" to="/projects"
          >Projects</g-link
        >
        <g-link class="pt-4 pb-8 block text-base font-medium" to="/images"
          >Images</g-link
        >
      </nav>
      <nav
        class="hidden py-6 md:block  md:flex md:text-base md:border-b-2 md:font-semibold"
      >
        <g-link class="pl-2 pr-6" to="/">About</g-link>
        <g-link class="px-6" to="/projects">Projects</g-link>
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
  @apply font-sans antialiased text-base text-cp1-900;
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
