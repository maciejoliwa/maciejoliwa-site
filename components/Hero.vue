<template>
  <section class="hero flex w-full h-screen p-4 flex-col items-center justify-center">
      <h1 class="text-4xl md:text-6xl py-2 px-8 text-center">Maciej Oliwa</h1>
      <p class="mt-2 text-xl md:text-2xl max-w-3xl text-center">
          I'm a young an ambitious developer based in <b>Poland, Kraków.</b> I'm mainly skilled in <b>JavaScript</b> and <b>TypeScript</b> with <b>Node.js.</b> I'm also learning 
          <b>C</b> in order to compile it to <b>WebAssembly</b> and use it on the web.
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
        background: linear-gradient(to bottom right, #f0f0f0, #fff);
        font-family: 'Darker Grotesque', sans-serif;
    }
</style>