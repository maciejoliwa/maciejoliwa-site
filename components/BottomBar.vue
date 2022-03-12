<template>
  <div class="bar absolute w-screen bottom-9 gap-4 hover:scale-105 flex items-center justify-center flex-row">
      <a v-for="social in socials" :key="social.link" :href="social.link">
          <img width="50px" :src="social.image_src" :alt="social.tooltip" :title="social.tooltip">
      </a>
  </div>
</template>

<script lang="ts">
interface Social {
    tooltip: string;
    image_src: string;
    link: string;
};

interface Socials {
    socials: Array<Social>;
};

export default {

    data(): Socials {
        return {socials: [
            { tooltip: "Check out my GitHub!", link: "https://github.com/maciejoliwa/", image_src: "github.svg" },
            { tooltip: "Check out my LinkedIN profile!", link: "https://www.linkedin.com/in/maciej-oliwa-a87bb6233/", image_src: "linkedin.webp" },
        ]}
    }

}
</script>

<style>

</style>