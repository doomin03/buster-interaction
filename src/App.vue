<template>
  <Intro></Intro>
  <Footer></Footer>
</template>

<script>
  import Intro from "@/components/Intro.vue";
  import Footer from "@/footer.vue"

  export default {
    name: "App",
    components: {
      Intro,
      Footer,
    }
  }
</script>
