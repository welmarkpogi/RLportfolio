<template>
  <div id="app" :class="{ 'dark-mode': darkMode }">
    <!-- Navbar -->
    <nav :class="{ 'navbar-dark bg-dark': !darkMode, 'navbar-light bg-light': darkMode }" class="navbar">
      <div class="container d-flex justify-content-between">
        <div class="d-flex flex-row"> <!-- Add class for flex row -->
          <router-link to="/" class="navbar-brand btn">Home</router-link>
          <router-link to="/contact" class="nav-link btn">Contact</router-link> 
          <router-link to="/about" class="nav-link btn">About</router-link> 
           
        </div>
        <div class="brightness-toggle" @click="toggleBrightness">
          <div class="toggle-switch" :class="{ 'light-mode': darkMode, 'dark-mode': !darkMode }"></div>
        </div>
      </div>
    </nav>
    <div class="sidebar">
      <!-- Sidebar content here if needed -->
    </div>
    <!-- Router View -->
    <router-view class="content"/>
    
    <!-- Footer -->
    <footer class="footer">
      <div class="d-flex justify-content-between align-items-center">
        <div class="social-icons">s
          <a href="#" class="social-icon">
            <img src="@/assets/fb1.png" alt="Facebook" class="icon">
          </a>
          <a href="#" class="social-icon">
            <img src="@/assets/twitter1.png" alt="Twitter" class="icon">
          </a>
          <a href="#" class="social-icon">
            <img src="@/assets/github1.png" alt="GitHub" class="icon">
          </a>
        </div>
        <p class="email-text" :class="{ 'light-text': darkMode }">Email: runelynbinuloac@gmail.com</p> <!-- Email address added -->
        <p>Created | at work by: artistmine</p>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      darkMode: false
    };
  },
  methods: {
    toggleBrightness() {
      this.darkMode = !this.darkMode;
    }
  }
};
</script>

<style>
#app {
  display: flex;
  flex-direction: column;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

.navbar {
  padding: 15px 0; 
}

.navbar-brand,
.nav-link {
  font-weight: bold;
  transition: transform 0.3s ease, color 0.3s ease;
  padding: 10px 20px; /* Add padding to create button-like appearance */
  border: none; /* Remove border */
  border-radius: 5px; /* Add border-radius for rounded corners */
  text-decoration: none; /* Remove default underline */
}

.nav-link:hover,
.navbar-brand:hover {
  transform: scale(1.1);
}

.router-link-exact-active {
  color: #1625ce !important;
}

.dark-mode .navbar-brand,
.dark-mode .nav-link {
  color: #fff; 
}

.dark-mode .router-link-exact-active {
  color: #1b1ba8 !important;
}

.sidebar {
  width: 200px;
  background-color: #f8f9fa;
}

.content {
  flex-grow: 1;
  display: flex;
  justify-content: center;
}

.footer {
  background-color: #343a40; /* Change footer background color to dark */
  padding: 20px;
}

.social-icons {
  display: flex;
  justify-content: center;
}

.social-icon {
  margin: 0 10px;
}

.icon {
  width: 24px; 
  height: 24px; 
}

.dark-mode .social-icon {
  color: #fff; 
}

.email-text {
  color: #edf1f4; /* Default text color */
}

.black-text {
  color: #fff; /* Text color for dark mode */
}

/* Responsive Styles */
@media (max-width: 768px) {
  .navbar {
    padding: 10px 0; 
  }

  .navbar-brand,
  .nav-link {
    font-size: 16px; 
  }
}

/* Toggle switch styles */
.brightness-toggle {
  display: flex;
  align-items: center;
  margin-right: 10px;
  cursor: pointer;
}

.toggle-switch {
  width: 40px;
  height: 20px;
  border-radius: 10px;
  background-color: #ddd; /* Default background color */
  position: relative;
  transition: background-color 0.3s;
}

.light-mode .toggle-switch {
  background-color: #fff; /* Light mode background color */
}

.dark-mode .toggle-switch {
  background-color: #570909; /* Dark mode background color */
}

.toggle-switch::after {
  content: '';
  position: absolute;
  width: 16px;
  height: 16px;
  border-radius: 50%;
  background-color: #fff;
  top: 2px;
  left: 2px;
  transition: transform 0.3s;
}

.dark-mode .toggle-switch::after {
  transform: translateX(20px); /* Move the switch to the right in dark mode */
}
</style>
