<template>
    <section id="skills" class="skills-section">
      <h2>Skills</h2>
      <div class="skills-list">
        <div class="skill">
          <img src="https://github.com/eviehammett/eviehammett.github.io/blob/dev/src/assets/logo.png?raw=true" alt="Vue.js"/>
          <p>Vue.js</p>
        </div>
        <!-- Add more skills as needed -->
      </div>
    </section>
  </template>
  
  <style scoped>
  .skills-section {
    padding: 3rem 1rem;
    background-color: #f5f5f5;
    text-align: center;
  }
  
  .skills-list {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 2rem;
  }
  
  .skill {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  
  .skill img {
    width: 50px;
    height: 50px;
  }
  
  .skill p {
    margin-top: 0.5rem;
    font-weight: bold;
  }
  </style>
  