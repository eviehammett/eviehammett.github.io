<template>
    <section id="contact" class="contact-section">
      <h2>Contact Me</h2>
      <form @submit.prevent="submitForm">
        <div class="form-group">
          <label for="name">Name</label>
          <input type="text" id="name" v-model="form.name" required/>
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" v-model="form.email" required/>
        </div>
        <div class="form-group">
          <label for="message">Message</label>
          <textarea id="message" v-model="form.message" required></textarea>
        </div>
        <button type="submit">Send</button>
      </form>
      <div class="social-links">
        <a href="https://www.linkedin.com/in/evie-hammett-67887b215/" target="_blank">LinkedIn</a>
        <a href="https://github.com/eviehammett" target="_blank">GitHub</a>
      </div>
    </section>
  </template>
  
  <script>
  export default {
    data() {
      return {
        form: {
          name: '',
          email: '',
          message: ''
        }
      }
    },
    methods: {
      submitForm() {
        // Handle form submission (e.g., send data to a server)
        alert('Form submitted');
      }
    }
  }
  </script>
  
  <style scoped>
  .contact-section {
    padding: 3rem 1rem;
    background-color: #f5f5f5;
    text-align: center;
  }
  
  .form-group {
    margin-bottom: 1rem;
  }
  
  label {
    display: block;
    margin-bottom: 0.5rem;
    font-weight: bold;
  }
  
  input, textarea {
    width: 100%;
    padding: 0.5rem;
    border: 1px solid #ddd;
    border-radius: 5px;
  }
  
  button {
    display: inline-block;
    padding: 0.75rem 1.5rem;
    background-color: #42b883;
    color: #ffffff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-weight: bold;
    transition: background-color 0.3s;
  }
  
  button:hover {
    background-color: #35495e;
  }
  
  .social-links a {
    display: inline-block;
    margin: 0 1rem;
    color: #42b883;
    text-decoration: none;
    font-weight: bold;
  }
  
  .social-links a:hover {
    text-decoration: underline;
  }
  </style>
  