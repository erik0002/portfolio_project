<template>
  <div class="flex flex-col h-screen">
    <Header/>
    <Nuxt class="flex-grow"/>
  </div>
</template>
<script>
import Header from "../components/app/Header";
export default {
  components: {Header}
}
</script>
