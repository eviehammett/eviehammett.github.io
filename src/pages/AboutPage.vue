<template>
    <section id="about" class="about-section">
      <img src="../assets/profile.jpg" alt="Profile Picture" class="profile-pic"/>
      <div class="about-content">
        <h2>About Me</h2>
        <p>[Your detailed introduction]</p>
        <a href="../assets/EvieCV.pdf" target="_blank" class="download-resume">Download Resume</a>
      </div>
    </section>
  </template>
  
  <style scoped>
  .about-section {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 3rem 1rem;
    background-color: #ffffff;
  }
  
  .profile-pic {
    width: 150px;
    height: 150px;
    border-radius: 50%;
    margin-bottom: 1.5rem;
  }
  
  .about-content {
    text-align: center;
  }
  
  .download-resume {
    display: inline-block;
    margin-top: 1rem;
    padding: 0.5rem 1.5rem;
    background-color: #42b883;
    color: #ffffff;
    border-radius: 5px;
    text-decoration: none;
    font-weight: bold;
    transition: background-color 0.3s;
  }
  
  .download-resume:hover {
    background-color: #35495e;
  }
  </style>
  