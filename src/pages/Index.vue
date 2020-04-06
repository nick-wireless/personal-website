<template>
  <Layout>
    <body>
      <p class="mt-12 sm:mt-8 md:mt-10 leading-relaxed">
        Hi! I'm Nick Hanigan from Darwin, Australia. Many people know me as the
        maker of Watashino Soap, the travel case for soap in your pocket.
      </p>
      <p class="mt-6 sm:mt-8 md:mt-10 leading-relaxed">
        I strive to be a creative, working on some cool things across very
        different time scales:
        <g-link class="link-internal">short</g-link> ,
        <g-link class="link-internal">medium</g-link> and
        <g-link class="link-internal">long</g-link>. I have an international
        work career focusing on development (property, independent manufacturing
        & fullstack programming). Prior to this, I sailed the seas and travelled
        the outback to earn an apprenticeship of sorts.
      </p>
      <p class="mt-6 sm:mt-8 md:mt-10 leading-relaxed">
        I rarely spend time on the socials and only check my personal inbox once
        every 2 weeks or so. That said, you can find a journal that somewhat
        describes 'me' by
        <g-link class="link-internal">photos here</g-link> and I am am available
        to <g-link class="link-internal">email direct here</g-link> anytime.
      </p>
      <p class="mt-6 sm:mt-8 md:mt-10 leading-relaxed">
        Every 12 monthis I intend to send out an insider's guide to my creative
        year. If I'm busy, I will send it every 6 months, to ensure it is always
        short and sweet. If you are interested,
        <g-link class="link-internal">subscribe here</g-link>
        <Link class="small-icon"></Link>.
      </p>
      <p class="mt-6 sm:mt-8 md:mt-10 leading-relaxed">
        Thanks for your interest. Have a great day!
      </p>
    </body>
  </Layout>
</template>

<script>
import Link from "~/assets/svgs/icon-external.svg";

export default {
  metaInfo: {
    title: "About"
  },
  components: {
    Link
  }
};
</script>

<style>
.link-internal {
  @apply text-cp1-1000 font-medium border-b border-cp1-1000;
}
.small-icon {
  @apply w-6 h-6;
}
</style>
