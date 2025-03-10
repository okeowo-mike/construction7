<template>
  <div class="nav-container" :class="{ 'scrolled-nav': isScrolled }">
    <div class="logo">
      <p>LOGO HERE</p>
    </div>
    <nav>
      <ul>
        <li><a class="nav-link" href="#about">ABOUT</a></li>
        <li><a class="nav-link" href="#our-projects">PROJECTS</a></li>
        <li><a class="nav-link" href="#footer">CONTACT</a></li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isScrolled: false,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll); // Important to prevent memory leaks
  },
  methods: {
    handleScroll() {
      this.isScrolled = window.scrollY > 50; // Adjust the scroll threshold as needed
    },
  },
};
</script>

<style scoped>
/* nav {
  a {
    font-weight: bold;
    color: #2c3e50;

    &.a-li-exact-active {
      color: #42b983;
    }
  }
} */
/* Apply border-box model and remove default margin/padding for all elements */
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.nav-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  position: fixed; /* or fixed if you want it to remain on scroll */
  top: 0;
  left: 0;
  width: 100%;
  z-index: 10;
  background: transparent; /* Initial transparent background */
  color: white;
  padding-top: 1rem;
  padding-bottom: 1rem;
  transition: background-color 0.3s ease; /* Smooth transition */
}

/* Add this style for the scrolled state */
.nav-container.scrolled-nav {
  background-color: rgba(
    0,
    0,
    0,
    0.5
  ); /* Slightly black transparent background */
}

.logo {
  padding-left: 40px;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  align-items: center;
  padding-right: 40px;
  gap: 1rem;
}
nav ul li {
  letter-spacing: 0.5px;
  font-family: "Times New Roman", Times, serif;
}

.nav-link {
  color: white;
  text-decoration: none;
}

.nav-link:hover {
  color: #d8d300;
}
</style>
