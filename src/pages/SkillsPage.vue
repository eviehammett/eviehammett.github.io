<template>
  <section id="skills" class="skills-section">
    <h2>Skills</h2>
    <div class="skills-list">
      <div class="skill" v-for="skill in skills" :key="skill.name">
        <div class="skill-card">
          <img :src="skill.logo" :alt="skill.name" />
          <p>{{ skill.name }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      skills: [
        { name: "HTML", logo: "https://upload.wikimedia.org/wikipedia/commons/6/61/HTML5_logo_and_wordmark.svg" },
        { name: "CSS", logo: "https://upload.wikimedia.org/wikipedia/commons/d/d5/CSS3_logo_and_wordmark.svg" },
        { name: "JavaScript", logo: "https://upload.wikimedia.org/wikipedia/commons/6/6a/JavaScript-logo.png" },
        { name: "Vue.js", logo: "https://github.com/eviehammett/eviehammett.github.io/blob/dev/src/assets/logo.png?raw=true" },
      ]
    };
  }
};
</script>

<style scoped>
.skills-section {
  padding: 4rem 1rem;
  background: linear-gradient(135deg, #ecf0f3, #dee2e6);
  text-align: center;
}

h2 {
  color: #35495e;
  font-size: 2rem;
  margin-bottom: 2rem;
}

.skills-list {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
  gap: 1.5rem;
  justify-content: center;
  max-width: 800px;
  margin: auto;
}

.skill-card {
  background: rgba(255, 255, 255, 0.2);
  backdrop-filter: blur(12px);
  padding: 1rem;
  border-radius: 12px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  text-align: center;
  border: 1px solid rgba(255, 255, 255, 0.3);
  transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.skill-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
}

.skill-card img {
  width: 60px;
  height: 60px;
  object-fit: contain;
  margin-bottom: 0.5rem;
}

.skill-card p {
  color: #555;
  font-weight: bold;
  font-size: 1rem;
}
</style>
