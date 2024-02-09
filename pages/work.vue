<template>
  <section class="blend-overlay flex h-full w-full flex-col content-center justify-center text-center font-serif">
    <div class="container mx-auto mb-12 mt-24 pl-8 pr-8 md:w-2/3 lg:w-1/2">
      <div class="relative mb-32 list-item cursor-pointer" v-for="(project, index) in projects" :key="index">
        <a :href="project.link" target="_blank" class="link text-white no-underline">
          <div v-if="project.awards" class="awards text mb-2 text-lg font-bold">
            {{ project.awards }}
          </div>
          <h2 class="title text-3xl font-bold no-underline md:text-4xl">
            {{ project.title }}
            <span class="year text-xl font-normal">{{ project.year }}</span>
          </h2>
          <div v-if="project.role" class="role mt-4 text-xl">
            {{ project.role }}
          </div>
          <div v-if="project.client" class="role text mt-4">
            {{ project.client }}
          </div>
          <!--<div v-if="project.tech" class="tech mt-4">{{project.tech}}</div>-->
          <div class="hover-container absolute inset-0 flex h-full w-full content-center items-center justify-center">
            <div class="hover-item work-item"></div>
          </div>
        </a>
      </div>
    </div>
  </section>
</template>
<script setup lang="ts">
  const projects = ref([
    {
      title: 'iMPAKT',
      year: '2019',
      role: 'Freelance Software Engineer',
      client: 'for Connected Health Innovation Centre',
      tech: 'Laravel, VueJS'
    },
    {
      title: 'Healthy Taps',
      year: '2018',
      role: 'Freelance Software Engineer',
      client: 'for National University of Ireland Galway',
      tech: 'Ionic, Firebase, Vue, Laravel, Google Cloud Engine'
    },
    {
      title: 'GreenX7',
      year: '2018',
      role: 'Lead Software Engineer',
      client: 'at Ply Studio',
      link: 'https://ply.studio'
    },
    {
      title: 'Apollo League',
      year: '2017',
      role: 'Lead Software Engineer',
      client: 'at Ply Studio',
      link: 'https://ply.studio'
    },
    {
      title: 'Adfomo',
      year: '2017',
      role: 'Lead Software Engineer',
      client: 'at Ply Studio',
      link: 'https://ply.studio'
    },
    {
      title: 'The Design Conference',
      year: '2017',
      role: 'Freelance Developer',
      client: 'for Analogue Digital',
      link: 'https://thedesignconference.com.au',
      tech: 'Wordpress, Braintree'
    },
    {
      title: 'Analogue Gallery',
      year: '2016',
      role: 'Freelance Developer',
      client: 'for Analogue Digital',
      tech: 'VanillaJS'
    },
    {
      title: 'First Coat Festival App',
      year: '2016',
      role: 'Freelance Developer',
      client: 'for Analogue Digital',
      link: 'https://firstcoat.com.au/',
      tech: 'Ionic, Angular, Silverstripe'
    },
    {
      title: 'The Design Conference App',
      awards: 'AGDA Design Awards 2016 - Winner - Digital Design',
      year: '2016',
      role: 'Freelance Developer / UX Designer',
      client: 'for Analogue Digital',
      link: 'http://awards2016.agda.com.au/finalist/3/10005/624',
      tech: 'Ionic, Angular, Silverstripe'
    },
    {
      title: 'Gray Matters',
      year: '2014-2016',
      role: 'Lead Developer & Data Scientist',
      client: 'at Ulster University',
      link: 'http://graymattersapp.org',
      tech: 'iOS, Android, Ionic, NodeJS, MongoDb, PHP, Matlab, SPSS'
    },
    {
      title: 'TAUT App',
      year: '2013',
      role: 'Lead Developer & Data Scientist',
      client: 'at Ulster University',
      link: 'https://link.springer.com/chapter/10.1007/978-3-319-13105-4_53',
      tech: 'Android, PHP, Matlab, R'
    }
  ])
</script>
