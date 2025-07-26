<template>
  <nav class="navbar">
    <div class="logo">Portfolio of Amelia</div>
    <div class="hamburger" @click="toggleMenu">
      ☰
    </div>
    <ul class="nav-links" :class="{ 'show': showMenu }">
      <li><a href="#Home">Home</a></li>
      <li><a href="#About">About</a></li>
      <li><a href="#Project">Project</a></li>
      <li><a href="#Contact">Contact</a></li>
    </ul>

    <div class="mel1">
      <button class="contact-btn">
        <a href="#Contact">Contact</a>
      </button>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      showMenu: false,
    };
  },
  methods: {
    toggleMenu() {
      this.showMenu = !this.showMenu;
    },
  },
};
</script>


<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 999;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 40px;
  background-color: #F0E4D3;
  border-bottom: 2px solid #d9cfc0;
}

.logo {
  font-weight: bold;
  font-size: 18px;
  color: black;
  margin-left: 20px;
}

.nav-links {
  display: flex;
  gap: 40px;
  list-style: none;
  padding: 0;
  margin: 0;
}

.nav-links a {
  text-decoration: none;
  color: black;
  font-weight: 500;
}

.mel1 {
  margin-right: 20px;
}

.contact-btn {
  background-color: #DCC5B2;
  border: none;
  padding: 8px 18px;
  border-radius: 6px;
  cursor: pointer;
  font-family: Poppins;
  font-weight: 600;
}

.contact-btn a {
  color: black;
  text-decoration: none;
  font-family: Poppins;
  font-weight: 600;
}

.hamburger {
  display: none;
  font-size: 24px;
  cursor: pointer;
}

@media (max-width: 768px) {
  .hamburger {
    display: block;
    margin-right: 20px;
  }

  .nav-links {
    display: none;
    flex-direction: column;
    gap: 20px;
    background-color: #f0e4d3;
    padding: 20px;
    position: absolute;
    top: 70px;
    left: 0;
    width: 100%;
  }

  .nav-links.show {
    display: flex;
  }

  .mel1 {
    display: none;
  }
}
</style>
