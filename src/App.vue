<template>
  <div id="app">
    <HeaderVue />
    <AboutPage />
    <SkillsPage />
    <ProjectsPage />
    <ContactPage />
    <FooterVue />
  </div>
</template>

<script>
import HeaderVue from './components/HeaderVue.vue';
import AboutPage from './pages/AboutPage.vue';
import SkillsPage from './pages/SkillsPage.vue';
import ProjectsPage from './pages/ProjectsPage.vue';
import ContactPage from './pages/ContactPage.vue';
import FooterVue from './components/FooterVue.vue';

export default {
  name: 'App',
  components: {
    HeaderVue,
    AboutPage,
    SkillsPage,
    ProjectsPage,
    ContactPage,
    FooterVue
  }
}
</script>

<style>
body {
  font-family: 'Roboto', sans-serif;
  margin: 0;
  background-color: #f5f5f5;
  color: #333;
}

a {
  color: #42b883;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}
</style>
