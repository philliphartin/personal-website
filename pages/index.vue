<template>
  <section
    class="blend-overlay min-h-screen w-full flex content-center justify-center font-serif flex-col text-center text-white"
  >
    <div class="container mx-auto md:w-1/2 pl-8 pr-8 mt-24 mb-12">
      <p class="md:text-xl mb-4">
        Thanks for visiting my little slice
        of the internet.
      </p>
      <p class="md:text-xl mb-4"></p>
      <p class="md:text-xl mb-4">
        I'm the Technical Director and Co-Founder of
        <a href="https://www.littlefox.studio" class="text-gray-400"
          >Littlefox Studio</a
        >, a venture studio, where we obsess over compelling digital products.
      </p>
      <p class="md:text-xl mb-6">
        My obsessing over work keeps me quite busy, but I'm always keen to hear about another interesting project, so don't hesitate to reach out over email or socials.
      </p>

      <a class="text-lg mx-2" href="mailto:phillip@littlefox.studio">
        <font-awesome-icon :icon="['fas', 'inbox']"></font-awesome-icon>
      </a>

      <a class="text-lg mx-2" href="https://www.linkedin.com/in/philliphartin/">
        <font-awesome-icon :icon="['fab', 'linkedin-in']"></font-awesome-icon>
      </a>

      <a class="text-lg mx-2" href="https://twitter.com/philliphartin">
        <font-awesome-icon :icon="['fab', 'twitter']"></font-awesome-icon>
      </a>
    </div>
  </section>
</template>

<script>
import styleMixin from './../mixin/style-mixin'

export default {
  mixins: [styleMixin],
  data() {
    return {}
  }
}
</script>
