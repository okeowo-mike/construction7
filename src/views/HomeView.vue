<template>
  <!-- <div class="home"> -->
  <HelloWorld />
  <NavBar />
  <!-- <WhatWeDo /> -->
  <AboutSection />
  <OurServices />
  <OurProjects />
  <OurClients />
  <MainFooter />
  <!-- </div> -->
</template>

<script>
import AboutSection from "@/components/about-section.vue";
import HelloWorld from "@/components/HelloWorld.vue";
import NavBar from "@/components/nav-bar.vue";
// import WhatWeDo from "@/components/what-we-do.vue";
import OurServices from "@/components/our-services.vue";
import OurProjects from "@/components/our-projects.vue";
import OurClients from "@/components/our-clients.vue";
import MainFooter from "@/components/Main-footer.vue";

// @ is an alias to /src

export default {
  name: "HomeView",
  components: {
    HelloWorld,
    NavBar,
    // WhatWeDo,
    AboutSection,
    OurServices,
    OurProjects,
    OurClients,
    MainFooter,
  },
};
</script>
