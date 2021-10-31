<template>
  <div>
    <Header />
    <section class="section">
      <div class="container">
        <main>
          <nuxt />
        </main>
      </div>
    </section>
    <Footer />
  </div>
</template>

<script>
import Header from '@/components/header.vue'
import Footer from '@/components/footer.vue'
export default {
  components: {
    Header,
    Footer
  }
}
</script>
