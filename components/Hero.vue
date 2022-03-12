<template>
  <section class="hero flex w-full h-screen bg-fuchsia-200 p-4 flex-col items-center justify-center">
      <h1 class="text-4xl md:text-6xl hover:animate-bounce">Maciej Oliwa</h1>
      <p class="mt-2 text-md md:text-2xl max-w-3xl md:text-center">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa quo atque aliquid rem quasi ut at facere fugiat, quibusdam quam obcaecati totam illum eligendi incidunt, eos ex autem. Sunt, laborum?
      </p>
      <projects :prop_projects="projects"/>
  </section>
</template>

<script lang="ts">
import Projects from './Projects.vue';

export default {
    name: "Hero",

    data() {
        return {
            projects: [
                "JavaScript",
                "TypeScript",
                "HTML",
                "CSS",
                "Vue",
                "Node.js",
                "MySQL",
                "Python",
                "Flask",
                "Selenium",
                "Clojure",
                "WebAssembly",
                "C",
                "Express.js"
            ]
        }
    },

    components: {
        Projects
    }
}
</script>

<style scoped>
    .hero {
        font-family: 'Darker Grotesque', sans-serif;
    }
</style>