<template>

  <Head>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="True">
    <link href="https://fonts.googleapis.com/css2?family=Merriweather&family=Montserrat&display=swap" rel="stylesheet">
    <title>
      Kevin Kretz
    </title>
  </Head>

  <!-- Hero -->
  <div class="hero min-h-screen" style="background-image: url(/adrien-olichon-SImgbUoEq8E-unsplash.jpg);">
    <!-- Background image by <a href="https://unsplash.com/@adrienolichon?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Adrien Olichon</a> on <a href="https://unsplash.com/photos/SImgbUoEq8E?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a> -->
    <div class="hero-overlay bg-opacity-60"></div>
    <div class="hero-content text-center text-neutral-content">
      <div class="max-w-xl">
        <div class="flex flex-row justify-center items-center gap-12 bg">
          <Avatar></Avatar>
          <div>
            <h1 class="mb-5 text-5xl font-bold text-left">Kevin Kretz</h1>
            <p class="mb-5 text-left">Provident cupiditate voluptatem et in. Quaerat fugiat ut assumenda excepturi
              exercitationem quasi.</p>
          </div>
        </div>
        <button class="btn btn-primary mt-6" @click="this.$refs['page'].scrollIntoView({ behavior: 'smooth' })">Learn
          more</button>
      </div>
    </div>
  </div>

  <!-- Content -->
  <div class="flex flex-col items-center p-4" ref="page">

    <!-- Social Media -->
    <div class="flex flex-col items-center max-w-7xl bg-secondary w-full m-4">
      <div class="">
        <p class="text-4xl lg:text-7xl m-4">@theKevinKretz</p>
        <div class="flex justify-evenly w-full m-4">
          <NuxtLink to="https://twitter.com/theKevinKretz">Twitter</NuxtLink>
          <NuxtLink to="https://www.linkedin.com/in/theKevinKretz/">LinkedIn</NuxtLink>
          <NuxtLink to="https://github.com/theKevinKretz">GitHub</NuxtLink>
        </div>
      </div>
    </div>

    <!-- Contact -->
    <div class="flex flex-col items-center max-w-7xl bg-secondary w-full m-4">
      <div class="text-4xl lg:text-7xl m-4">
        <NuxtLink to="mailto:mail@kevinkretz.de">mail@kevinkretz.de</NuxtLink>
      </div>
    </div>

    <!-- Internships -->
    <div class="flex flex-col items-center m-4">
      <h2 class="text-3xl">Internships</h2>
      <div class="max-w-7xl">
        <div class="grid grid-cols-1 lg:grid-cols-2 gap-3 p-3">
          <Card v-for="(intern, index) in interns" v-bind="intern" :key="index" class="w-full h-1/2" />
        </div>
      </div>
    </div>
  </div>

  <Footer></Footer>
</template>

<script setup lang="ts">
let banners = ref(["hello", "world"]);
let interns = ref(
  [
    {
      company: "SAP SE",
      description: "SAP Desc",
      logo_url: "https://www.sap.com/content/dam/application/shared/logos/sap-logo-svg.svg"
    },
    {
      company: "Testo",
      description: "Testo Desc",
      logo_url: "https://upload.wikimedia.org/wikipedia/commons/1/12/Logo_testo.jpg"
    }
  ]
);
</script>