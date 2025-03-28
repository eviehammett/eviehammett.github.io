<template>
  <section id="projects" class="projects-section">
    <h2>Projects</h2>
    <div class="projects-grid">
      <div class="project-card" v-for="project in projects" :key="project.id">
        <img :src="project.image" :alt="project.name" class="project-image" />
        <div class="project-info">
          <h3>{{ project.name }}</h3>
          <p>{{ project.description }}</p>
          <div class="project-links">
            <a :href="project.liveDemo" target="_blank" class="project-btn live-demo">Live Demo</a>
            <a :href="project.github" target="_blank" class="project-btn github">GitHub</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          id: 1,
          name: 'Pomodoro Timer',
          description: 'A pomodoro timer app with custom theme settings.',
          image: 'https://github.com/eviehammett/eviehammett.github.io/blob/dev/public/pomodoro.png?raw=true',
          liveDemo: 'https://eviepomodorotimer.netlify.app',
          github: 'https://github.com/eviehammett/pomodoro'
        },
        {
          id: 2,
          name: 'Project 2',
          description: 'Description of Project 2',
          image: '#',
          liveDemo: 'link',
          github: 'link'
        }
      ]
    };
  }
};
</script>

<style scoped>
.projects-section {
  padding: 4rem 1rem;
  background: linear-gradient(135deg, #ecf0f3, #dee2e6);
  text-align: center;
}

h2 {
  color: #35495e;
  font-size: 2rem;
  margin-bottom: 2rem;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 2rem;
  justify-content: center;
  max-width: 1000px;
  margin: auto;
}

.project-card {
  background: rgba(255, 255, 255, 0.2);
  backdrop-filter: blur(12px);
  border-radius: 15px;
  overflow: hidden;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
}

.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
}

.project-image {
  width: 180px;
  height: 180px;
  object-fit: cover;
  border-bottom: 1px solid rgba(255, 255, 255, 0.2);
}

.project-info {
  padding: 1.5rem;
  text-align: center;
}

.project-info h3 {
  color: #35495e;
  font-size: 1.5rem;
  margin-bottom: 0.5rem;
}

.project-info p {
  color: #555;
  font-size: 1rem;
  margin-bottom: 1rem;
}

.project-links {
  display: flex;
  justify-content: center;
  gap: 1rem;
}

.project-btn {
  display: inline-block;
  padding: 0.6rem 1.2rem;
  border-radius: 8px;
  text-decoration: none;
  font-weight: bold;
  transition: background-color 0.3s ease-in-out;
}

.live-demo {
  background-color: #42b883;
  color: #fff;
}

.github {
  background-color: #35495e;
  color: #fff;
}

.project-btn:hover {
  opacity: 0.8;
}
</style>
