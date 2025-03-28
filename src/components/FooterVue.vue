<template>
  <footer class="footer">
    <p>&copy; 2025 Evie Hammett. All rights reserved.</p>
  </footer>
</template>

<style scoped>
.footer {
  width: 100%;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  padding: 1rem 0;
  text-align: center;
  font-size: 0.9rem;
  font-weight: bold;
  color: #35495e;
  box-shadow: 0 -2px 10px rgba(0, 0, 0, 0.1);
  position: relative;
  bottom: 0;
}

.footer p {
  margin: 0;
  transition: color 0.3s ease-in-out;
}

.footer p:hover {
  color: #42b883;
}
</style>
