<template>
  <header ref="header" class="py-6">
    <div class="flex items-center justify-between">
      <ul class="flex">
        <li class="ml-12">
          <NuxtLink to="/">Main</NuxtLink>
        </li>
        <li class="ml-12">
          <NuxtLink to="/home">Home</NuxtLink>
        </li>
        <li class="ml-12">
          <NuxtLink to="/services">Services</NuxtLink>
        </li>
        <li class="ml-12">
          <NuxtLink to="/skills">Skills</NuxtLink>
        </li>
        <li class="ml-12">
          <NuxtLink to="/projects">Projects</NuxtLink>
        </li>
      </ul>

      <VBurgerMenu :closeOnNavigation="true" right v-if="isMobile">
        <div class="ml-12">
          <NuxtLink to="/">Main</NuxtLink>
        </div>
        <div class="ml-12">
          <NuxtLink to="/home">Home</NuxtLink>
        </div>
        <div class="ml-12">
          <NuxtLink to="/services">Services</NuxtLink>
        </div>
        <div class="ml-12">
          <NuxtLink to="/skills">Skills</NuxtLink>
        </div>
        <div class="ml-12">
          <NuxtLink to="/projects">Projects</NuxtLink>
        </div>

      </VBurgerMenu>
    </div>
  </header>
</template>
<script>

export default  {
  name: 'Header',
  components: {

  },
  data() {
    return {
      isMobile: false
    }
  },
  computed: {},
  methods: {
    onResize() {
      this.isMobile = window.innerWidth < 850 ? true : false
    }
  },
  mounted() {
    this.onResize()
    window.addEventListener('resize', this.onResize)
  },
  beforeDestroy() {
    window.removeEventListener('resize', this.onResize)
  }
}
</script>
