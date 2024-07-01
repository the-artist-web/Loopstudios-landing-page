<template>
  <Header />
  <main>
    <article>
      <Hero />
      <About />
      <BoxList />
    </article>
  </main>
  <Footer />
</template>

<script>
import Header from "@/views/Header.vue"
import Hero from "@/views/Hero.vue"
import About from "@/views/About.vue"
import BoxList from "@/views/BoxList.vue"
import Footer from "@/views/Footer.vue"

export default {
  name: 'App',
  components: {
    Header,
    Hero,
    About,
    BoxList,
    Footer
  }
}
</script>

<style>
#app {
  width: 100%;
  height: auto;
  display: flex;
  flex-direction: column;
}
</style>
