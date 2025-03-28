<template>
  <section id="about" class="about-section">
    <div class="about-container">
      <img :src="profilePic" alt="Profile Picture" class="profile-pic" />
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
        <p>Let's get in touch and explore how I can help bring your vision to life!</p>
        <div class="button-section">
          <a href="#contact" class="view-buttons contact-me">Contact Me!</a>
          <a :href="cvLink" target="_blank" class="view-buttons">View My Resume</a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      profilePic: 'https://raw.githubusercontent.com/eviehammett/eviehammett.github.io/dev/src/assets/profile.jpg',
      cvLink: 'https://drive.google.com/file/d/1CGt3eDsPWmOD-FYpbrPM1_OZOk7uvLbV/view?usp=drive_link'
    }
  },
}
</script>

<style scoped>
.about-section {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 4rem 1rem;
  background: linear-gradient(135deg, #f8f9fa, #e9ecef);
}

.about-container {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 2rem;
  background: white;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  max-width: 900px;
  width: 90%;
}

.profile-pic {
  width: 180px;
  height: 180px;
  border-radius: 50%;
  border: 4px solid #42b883;
  object-fit: cover;
}

.about-content {
  text-align: left;
  width: 100%;
}

h2 {
  color: #35495e;
  font-size: 2rem;
  margin-bottom: 1rem;
}

p {
  color: #555;
  line-height: 1.6;
  margin-bottom: 1rem;
}

.button-section {
  margin-top: 1.5rem;
}

.view-buttons {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  border-radius: 8px;
  font-weight: bold;
  text-decoration: none;
  transition: background-color 0.3s, transform 0.2s;
  background: #42b883;
  color: white;
  box-shadow: 0 4px 6px rgba(66, 184, 131, 0.3);
}

.view-buttons:hover {
  background: #35495e;
  transform: translateY(-2px);
}

.contact-me {
  margin-right: 1rem;
}

/* Responsive Design */
@media (max-width: 768px) {
  .about-container {
    flex-direction: column;
    text-align: center;
  }

  .profile-pic {
    width: 150px;
    height: 150px;
  }
}
</style>
