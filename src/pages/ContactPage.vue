<template>
  <section id="contact" class="contact-section">
    <div class="contact-container">
      <h2>Contact Me</h2>
      <form @submit.prevent="submitForm" class="contact-form">
        <div class="form-group">
          <label for="name">Name</label>
          <input type="text" id="name" v-model="form.name" required />
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" v-model="form.email" required />
        </div>
        <div class="form-group">
          <label for="message">Message</label>
          <textarea id="message" v-model="form.message" required></textarea>
        </div>
        <button type="submit">Send Message</button>
      </form>
      <div class="social-links">
        <a href="https://www.linkedin.com/in/evie-hammett-67887b215/" target="_blank">LinkedIn</a>
        <a href="https://github.com/eviehammett" target="_blank">GitHub</a>
      </div>
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
      alert('Form submitted');
    }
  }
}
</script>

<style scoped>
.contact-section {
  padding: 4rem 1rem;
  background: linear-gradient(135deg, #42b883, #35495e);
  color: white;
  display: flex;
  justify-content: center;
  align-items: center;
}

.contact-container {
  background: white;
  color: #333;
  padding: 2rem;
  border-radius: 12px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  width: 90%;
  max-width: 500px;
  text-align: center;
}

h2 {
  margin-bottom: 1rem;
  color: #35495e;
  font-size: 1.8rem;
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  margin: auto;
}

.form-group {
  text-align: left;
  margin-right: 25px;
}

label {
  display: block;
  font-weight: bold;
  margin-bottom: 0.5rem;
  color: #35495e;
}

input, textarea {
  width: 100%;
  padding: 0.75rem;
  border: 1px solid #ddd;
  border-radius: 6px;
  font-size: 1rem;
  transition: border-color 0.3s;
  margin: auto;
}

input:focus, textarea:focus {
  border-color: #42b883;
  outline: none;
}

textarea {
  height: 120px;
  resize: vertical;
}

button {
  background: #42b883;
  color: white;
  padding: 0.75rem;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  font-size: 1rem;
  font-weight: bold;
  transition: background 0.3s;
}

button:hover {
  background: #35495e;
}

.social-links {
  margin-top: 1.5rem;
}

.social-links a {
  color: #42b883;
  font-weight: bold;
  text-decoration: none;
  margin: 0 0.75rem;
  transition: color 0.3s;
}

.social-links a:hover {
  color: #35495e;
  text-decoration: underline;
}
</style>
