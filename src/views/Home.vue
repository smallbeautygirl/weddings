<template>
  <div>
    <Navbar />
    <Masthead />
    <Service />
    <Registration />
    <Video />
    <Team />
    <!-- <Footer /> -->
  </div>
</template>

<script>
import Navbar from "../components/Navbar.vue";
import Masthead from "../components/Masthead.vue";
import Service from "../components/Service.vue";
import Registration from "../components/Registration.vue";
import Video from "../components/Video.vue";
import Team from "../components/Team.vue";
// import Footer from "../components/Footer.vue";

export default {
  name: "Home",

  components: {
    Navbar,
    Masthead,
    Service,
    Registration,
    Video,
    Team,
    // Footer,
  },
};
</script>
