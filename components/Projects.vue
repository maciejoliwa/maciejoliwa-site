<template>
  <section class="projects mt-2 md:mt-6 text-center md:max-w-2xl xl:max-w-6xl">
      <div class="text-md select-none md:text-xl inline-block hover:text-pink-600 transition-all hover:font-bold duration-500" v-for="(project, index) in projects" :key="project.id">
          {{ project }}
          <span class="text-black" v-if="!isLast(index)">&nbsp;●&nbsp;</span>
      </div>
  </section>
</template>

<script lang="ts">

interface ProjectsData {
    projects: Array<string>
}

export default {
    name: 'Projects',

    props: ["prop_projects"],

    data(): ProjectsData {
        return {
            //@ts-ignore
            projects: this.prop_projects
        }
    },

    methods: {

        isLast(index: number): boolean {
            //@ts-ignore
            return (index == (this.projects.length - 1));
        },

    }
}
</script>

<style>

</style>