<template>
    <section id="about" class="about-section">
      <img :src="profilePic" alt="Profile Picture" class="profile-pic"/>
      <div class="about-content">
        <h2>About Me</h2>
        <p>Welcome to my portfolio! I'm a passionate Software Developer specializing in front-end development. With a degree in 
          Multimedia Software Development from MCAST, I have a solid foundation in software engineering, multimedia design, and user 
          experience.</p>
        <p>My professional journey has taken me from technical support to front-end development at Arkafort, where I honed my 
          problem-solving skills and customer-centric approach. As a Junior Front-End Developer, I've worked on key projects using 
          HTML, CSS, JavaScript, Vue.js, and Node.js to create dynamic, user-friendly interfaces. I'm also experienced with 
          GitLab for version control and collaboration, and proficient in WordPress and Elementor for responsive web design.</p>
        <p>I'm always seeking new opportunities to grow and apply my skills in innovative environments. I'm excited to contribute to 
          projects that embrace cutting-edge technologies and collaborative team dynamics.</p>
        <p>Let's connect and explore how I can help bring your vision to life!</p>
        <div class="button-section">
          <a href="#contact" class="view-buttons contact-me">Contact Me!</a>
          <a :href="cvLink" target="_blank" class="view-buttons">View My Resume</a>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    data() {
      return {
        profilePic: 'https://raw.githubusercontent.com/eviehammett/eviehammett.github.io/dev/src/assets/profile.jpg',
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
    width: 75%;
    margin: auto;
  }
  
  .view-buttons {
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

  .contact-me {
    margin-right: 4rem;
  }
  
  .view-resume:hover {
    background-color: #35495e;
  }
  </style>
  