<template>
  <header class="header">
    <nav class="nav">
      <div class="logo">Evie Hammett</div>
      <button class="menu-toggle" @click="toggleMenu">
        <span :class="{ open: menuOpen }"></span>
        <span :class="{ open: menuOpen }"></span>
        <span :class="{ open: menuOpen }"></span>
      </button>
      <ul :class="['nav-list', { open: menuOpen }]">
        <li><a href="#about" @click.prevent="smoothScroll('about')">About</a></li>
        <li><a href="#skills" @click.prevent="smoothScroll('skills')">Skills</a></li>
        <li><a href="#projects" @click.prevent="smoothScroll('projects')">Projects</a></li>
        <li><a href="#contact" @click.prevent="smoothScroll('contact')">Contact</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  data() {
    return {
      menuOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.menuOpen = !this.menuOpen;
    },
    closeMenu() {
      this.menuOpen = false;
    },
    smoothScroll(targetId) {
      const targetElement = document.getElementById(targetId);
      if (targetElement) {
        targetElement.scrollIntoView({
          behavior: "smooth",
          block: "start"
        });
      }
      this.closeMenu(); // Close menu after clicking (on mobile)
    }
  }
};
</script>

<style scoped>
/* Header */
.header {
  width: 100%;
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  padding-top: 1rem;
  padding-bottom: 1rem;
  position: sticky;
  top: 0;
  left: 0;
  z-index: 1000;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

/* Navigation */
.nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1200px;
  margin: auto;
  padding: 0 1rem;
}

/* Logo */
.logo {
  font-size: 1.5rem;
  font-weight: bold;
  color: #35495e;
}

/* Desktop Navigation */
.nav-list {
  display: flex;
  list-style: none;
  gap: 1.5rem;
  transition: transform 0.3s ease-in-out;
}

.nav-list a {
  text-decoration: none;
  color: #35495e;
  font-weight: bold;
  transition: color 0.3s ease;
}

.nav-list a:hover {
  color: #42b883;
}

/* Mobile Menu Button */
.menu-toggle {
  display: none;
  background: none;
  border: none;
  cursor: pointer;
  flex-direction: column;
  gap: 6px;
  width: 35px;
  height: 30px;
  position: relative;
  margin-right: 20px;
}

.menu-toggle span {
  display: block;
  width: 100%;
  height: 4px;
  background: #35495e;
  transition: all 0.3s ease-in-out;
}

/* Open State */
.menu-toggle span.open:nth-child(1) {
  transform: translateY(8px) rotate(45deg);
}
.menu-toggle span.open:nth-child(2) {
  opacity: 0;
}
.menu-toggle span.open:nth-child(3) {
  transform: translateY(-8px) rotate(-45deg);
}

/* Responsive Styles */
@media (max-width: 768px) {
  .menu-toggle {
    display: flex;
  }

  .nav-list {
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    background: rgba(0, 0, 0, 0.9);
    flex-direction: column;
    align-items: center;
    padding: 1rem 0;
    transform: translateY(-200%);
    transition: transform 0.3s ease-in-out;
  }

  .nav-list a {
    color: #ffffff;
  }

  .nav-list.open {
    transform: translateY(0);
  }

  .nav-list li {
    padding: 1rem 0;
  }
}
</style>