<!-- A framework like bootstrap handles all of the CSS side and provides us with easy to use classes -->
<!-- BootstrapVue provides several convenient functional components tailored for layout, which can simplify your complex page markup compared to traditional Bootstrap v4 markup. Feel free to switch back and forth between traditional Bootstrap v4 markup (i.e. <div>s and classes) and BootstrapVue's convenient functional layout components. -->



<template>
  <div id="app">


    <Navigation :name="name" />

    <!-- p-0 for padding -->
    <!-- Use <b-container> for a responsive pixel width or <b-container fluid> for width: 100% across all viewport and device sizes. -->


    <b-container class="p-0" fluid>
      <About :name="name" />
      <Border />
      <Experience />
      <Border />
      <Skills />
      <Border />
      <Projects />
      <Border />
      <Education />
      <Border />
      <Awards />
    </b-container>

  </div>
</template>

<script>
import smoothScroll from 'smooth-scroll';

import About from "@/components/About";
import Experience from "@/components/Experience";
import Education from "@/components/Education";
import Skills from "@/components/Skills";
import Projects from "@/components/Projects";
import Awards from "@/components/Awards";
import Navigation from "@/components/Navigation";
import Border from "@/components/Border";

export default {
  name: "app",
  data() {
    return {
      name: {
        first: "Augustas",
        last: "Juskevicius"
      }
    }
  },
  components: {
    About,
    Experience,
    Education,
    Skills,
    Projects,
    Awards,
    Navigation,
    Border
  },
  created: function() {
    var scroll = new smoothScroll('a[href*="#"]', {
      updateURL: false
    })
  }
};
</script>
