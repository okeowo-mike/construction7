<template>
  <nav>
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </nav>
  <div id="cursor-trail" :style="trailStyle"></div>
  <router-view />
</template>

<!-- ///////////////////////////////////////////////// -->
<script>
export default {
  data() {
    return {
      trailStyle: {
        transform: "translate(-50%, -50%)",
      },
    };
  },
  mounted() {
    document.addEventListener("mousemove", this.updateTrailPosition);
  },
  beforeUnmount() {
    document.removeEventListener("mousemove", this.updateTrailPosition);
  },
  methods: {
    updateTrailPosition(event) {
      const x = event.clientX;
      const y = event.clientY;
      this.trailStyle = {
        transform: `translate(-65%, -150%) translate(${x}px, ${y}px)`, // Added px to both x and y
      };
    },
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

html {
  scroll-behavior: smooth;
}

/* Hide scrollbar for Chrome, Safari and Edge */
::-webkit-scrollbar {
  width: 0px; /* Or height: 0px; for horizontal scrollbars */
  background: transparent; /* Optional: just make scrollbar invisible */
}

// ///////////////////////////////////
/* Apply border-box model and remove default margin/padding for all elements */
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

// /////////////////////////////////////////////
#cursor-trail {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  border: 1px solid #d8d300;
  background-color: transparent;
  position: fixed;
  pointer-events: none;
  z-index: 9999;
  transform: translate(-50%, -50%);
  transition: transform 0.2s ease-out;
  transform-origin: center;
}
</style>
