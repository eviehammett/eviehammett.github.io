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
        <button type="submit" class="send-btn">Send Message</button>
      </form>
      <div class="social-links">
        <a href="https://www.linkedin.com/in/evie-hammett-67887b215/" target="_blank" class="social-icon linkedin">
          <img src="https://cdn-icons-png.flaticon.com/512/174/174857.png" alt="LinkedIn" />
        </a>
        <a href="https://github.com/eviehammett" target="_blank" class="social-icon github">
          <img src="https://cdn-icons-png.flaticon.com/512/25/25231.png" alt="GitHub" />
        </a>
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
    };
  },
  methods: {
    submitForm() {
      // Construct the mailto link with form details
      const subject = 'Contact Form Submission';
      const body = `Name: ${this.form.name}\nEmail: ${this.form.email}\n\nMessage:\n${this.form.message}`;
      const mailtoLink = `mailto:eviehammett@gmail.com?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;

      // Open the user's email client with the prefilled information
      window.location.href = mailtoLink;

      // Reset form details
      this.form.name = '';
      this.form.email = '';
      this.form.message = '';
    }
  }
};
</script>

<style scoped>
.contact-section {
  padding: 4rem 1rem;
  background: linear-gradient(135deg, #ecf0f3, #dee2e6);
  display: flex;
  justify-content: center;
  align-items: center;
}

.contact-container {
  background: rgba(255, 255, 255, 0.2);
  backdrop-filter: blur(12px);
  color: #333;
  padding: 2.5rem;
  border-radius: 15px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
  width: 90%;
  max-width: 500px;
  text-align: center;
}

h2 {
  margin-bottom: 1.5rem;
  color: #35495e;
  font-size: 2rem;
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.form-group {
  text-align: left;
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
  border: none;
  border-radius: 8px;
  font-size: 1rem;
  transition: all 0.3s;
  background: rgba(255, 255, 255, 0.6);
  box-shadow: inset 2px 2px 5px rgba(0, 0, 0, 0.05);
}

input:focus, textarea:focus {
  outline: none;
  border: 2px solid #42b883;
}

textarea {
  height: 120px;
  resize: vertical;
}

.send-btn {
  background: #42b883;
  color: white;
  padding: 0.75rem;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  font-size: 1rem;
  font-weight: bold;
  transition: background 0.3s ease-in-out, transform 0.2s;
}

.send-btn:hover {
  background: #35495e;
  transform: scale(1.05);
}

.social-links {
  margin-top: 2rem;
  display: flex;
  justify-content: center;
  gap: 1.5rem;
}

.social-icon img {
  width: 40px;
  height: 40px;
  transition: transform 0.3s ease-in-out;
}

.social-icon:hover img {
  transform: scale(1.1);
}
</style>
