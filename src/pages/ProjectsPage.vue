<template>
    <section id="projects" class="projects-section">
      <h2>Projects</h2>
      <div class="projects-grid">
        <div class="project-card" v-for="project in projects" :key="project.id">
          <img :src="project.image" :alt="project.name" style="height: 120px; width: 120px;"/>
          <div class="project-info">
            <h3>{{ project.name }}</h3>
            <p>{{ project.description }}</p>
            <a :href="project.liveDemo" target="_blank">Live Demo</a>
            <a :href="project.github" target="_blank">GitHub</a>
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
          },
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .projects-section {
    padding: 3rem 1rem;
    background-color: #ffffff;
    text-align: center;
  }
  
  .projects-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 2rem;
  }
  
  .project-card {
    width: 300px;
    border: 1px solid #ddd;
    border-radius: 8px;
    overflow: hidden;
    transition: transform 0.3s;
  }
  
  .project-card:hover {
    transform: translateY(-10px);
  }
  
  .project-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }
  
  .project-info {
    padding: 1rem;
  }
  
  .project-info h3 {
    margin-top: 0;
  }
  
  .project-info a {
    display: block;
    margin-top: 0.5rem;
    color: #42b883;
    text-decoration: none;
    font-weight: bold;
  }
  
  .project-info a:hover {
    text-decoration: underline;
  }
  </style>
  