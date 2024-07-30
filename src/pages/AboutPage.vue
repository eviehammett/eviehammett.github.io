<template>
    <section id="about" class="about-section">
      <img :src="profilePic" alt="Profile Picture" class="profile-pic"/>
      <div class="about-content">
        <h2>About Me</h2>
        <p>[Your detailed introduction]</p>
        <a :href="cvLink" target="_blank" class="view-resume">View My Resume</a>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    data() {
      return {
        profilePic: 'https://github.com/eviehammett/eviehammett.github.io/blob/main/src/assets/profile.jpg',
        cvLink: 'https://drive.google.com/file/d/1GD99SyJWTl-mKvxMnWnab189iQSuXjEQ/view?usp=drive_link'
      }
    },
  }
  </script>
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
  
  .view-resume {
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
  
  .view-resume:hover {
    background-color: #35495e;
  }
  </style>
  