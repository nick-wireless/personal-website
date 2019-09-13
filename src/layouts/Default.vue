<template>
  <div class="max-w-3xl mx-auto px-6 md:px-8">
    <header class="text-cp1-800 pt-10">
      <div class="flex justify-between items-center">
        <g-link class="text-lg font-semibold" to="/">Nick Hanigan</g-link>
        <div class="block md:hidden">Menu</div>
      </div>
      <nav class="nav hidden md:block">
        <g-link class="nav__link" to="/">About</g-link>
        <g-link class="nav__link" to="/blog">Blog</g-link>
        <g-link class="nav__link" to="/blog">Images</g-link>
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

<style>
body {
  @apply font-sans antialiased bg-cp2-100 text-cp1-800;
}

.nav__link {
  @apply text-cp1-1000;
}
</style>
