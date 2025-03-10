<template>
  <section id="our-projects" class="our-projects">
    <div class="our-project-texts">
      <p class="what-we-do">What We Do</p>
      <h2>Our Projects</h2>
      <p class="what-we-do-p2">
        I'm a paragraph. Click here to add your own text and edit me. I’m a great place for you to
        tell a story and let your users know a little more about you.
      </p>
    </div>
    <div class="gallery-container">
      <button @click="prevImage" class="arrow-button">
        <span class="arrow">‹</span>
      </button>

      <div v-for="(image, index) in visibleImages" :key="index" class="image-container">
        <img :src="image" :alt="'Image ' + (startIndex + index + 1)" />
      </div>

      <button @click="nextImage" class="arrow-button">
        <span class="arrow">›</span>
      </button>
    </div>
  </section>
</template>

<!-- ////////////////////////////////// -->
<script>
import img1 from '../assets/wwd-3.jpg';
import img2 from '../assets/wwd-2.jpg';
import img3 from '../assets/wwd-1.jpg';
import img4 from '../assets/wwd-4.jpg';
import img5 from '../assets/project-img-5.jpeg';
import img6 from '../assets/project-img-6.jpeg';
import img7 from '../assets/project-img-7.jpg';

export default {
  data() {
    return {
      images: [
        img1,
        img2,
        img3,
        img4,
        img5,
        img6,
        img7,
        img2, // Duplicate of img2
      ],
      startIndex: 0,
      activeIndex: 0,
    };
  },
  computed: {
    visibleImages() {
      return this.images.slice(this.startIndex, this.startIndex + 3);
    },
  },
  methods: {
    nextImage() {
      if (this.startIndex + 3 < this.images.length) {
        this.startIndex += 1;
        this.activeIndex = Math.min(this.activeIndex + 1, 3);
      }
    },
    prevImage() {
      if (this.startIndex > 0) {
        this.startIndex -= 1;
        this.activeIndex = Math.max(this.activeIndex - 1, 0);
      }
    },
  },
};
</script>

<style scoped>
.our-project-texts {
  margin: 0 3rem;
  margin-top: 10rem;
  max-width: 700px;
  text-align: left;
}

.what-we-do {
  margin-bottom: 1rem;
  font-weight: 300;
  font-size: 30px;
  text-align: left;
}

.our-project-texts h2 {
  font-size: 3rem;
  font-weight: 500;
  line-height: 50px;
  color: #d8d300;
  text-align: left;
}

.what-we-do-p2 {
  padding-top: 0.5rem;
  max-width: 650px;
}

/* /////////////////////////////////// */
.gallery-container {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 5px;
  margin-top: 3rem;
}

.image-container {
  display: inline-block; /* Or your preferred layout */
  margin: 5px;
}
.image-container img {
  width: 300px;
  height: 500px;
  object-fit: cover;
  border-radius: 20px;
}

.arrow {
  background: none;
  border: none;
  font-size: 24px;
  cursor: pointer;
}

.gallery {
  display: flex;
  gap: 5px;
  overflow: hidden;
  padding: 2rem 0;
}

.gallery-item {
  width: 270px;
  height: 490px;
  margin: auto 0.5rem;
  transition: transform 0.3s ease-in-out;
}

.gallery-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 20px;
}

.active {
  transform: scale(1.1);
  width: 310px;
  height: 490px;
}

/* /////////////////////////////////////////////////// */
.arrow-button {
  width: 60px; /* Adjust size as needed */
  height: 60px; /* Adjust size as needed */
  border-radius: 50%; /* Creates the circle */
  background-color: transparent; /* Light gray background, adjust to your theme */
  border: 1px black solid; /* Remove default button border */
  cursor: pointer;
  display: inline-flex; /* Center content horizontally and vertically */
  align-items: center;
  justify-content: center;
  transition: background-color 0.2s ease; /* Smooth hover effect */
  margin: 5px; /* Add some spacing between the buttons */
}

.arrow-button:hover {
  background-color: #f4f4f4; /* Slightly darker background on hover */
}

.arrow {
display: flex;
justify-content: center;
align-items: center;
  font-size: 20px; /* Adjust arrow size as needed */
  color: #333; /* Dark gray arrow color, adjust to your theme */
  line-height: 0; /* Removes default line height */
}
</style>
