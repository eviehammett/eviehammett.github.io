<template>
    <section id="home" class="home-section">
      <div class="intro">
        <h1>Hello, I'm [Your Name]</h1>
        <p>Junior Frontend Developer specializing in Vue.js</p>
        <a href="#projects" class="cta">View My Work</a>
      </div>
    </section>
  </template>
  
  <style scoped>
  .home-section {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    
    color: #ffffff;
    text-align: center;
  }
  
  .cta {
    display: inline-block;
    padding: 1rem 2rem;
    margin-top: 1rem;
    background-color: #42b883;
    color: #ffffff;
    border: none;
    border-radius: 5px;
    text-transform: uppercase;
    font-weight: bold;
    cursor: pointer;
    transition: background-color 0.3s;
  }
  
  .cta:hover {
    background-color: #35495e;
  }
  </style>
  