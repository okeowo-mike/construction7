<template>
  <div class="container">
    <div class="hero">
      <video autoplay loop muted playsinline class="hero-video">
        <source src="../assets/hero-video-3.mp4" type="video/mp4" />
        Your browser does not support the video tag.
      </video>
      <div class="hero-content">
        <h1>WELCOME TO MY CONSTRUCTION SITE</h1>
        <p class="hero-text-1">
          Some captivating text about your amazing product or service
        </p>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Ducimus
          exercitationem libero doloribus neque.
        </p>
        <button class="hero-learn-btn">Learn More</button>
      </div>
    </div>

    <!-- ///////////////////////////////////// -->
    <section class="content-section">
      <div id="what-we-do" class="what-we-do">
        <div class="service-texts">
          <div class="service-text-1">
            <p class="service-p1">Building Is What We Do</p>
            <h2>MCR Construction Is Leading Quality Projects</h2>
            <!-- <p>
            I'm a paragraph. Click here to add your own text and edit me. Let your
            users get to know you.
          </p> -->
          </div>
          <div class="service-text-2">
            <div class="services-btn">
              <button>Read More</button>
            </div>
          </div>
        </div>

        <div class="pic-card-1">
          <div class="card commercial-text">
            <div class="litlle-line"></div>
            <h3>Commercial</h3>
            <p>
              I’m a paragraph. Click here to add your own text and edit me. It’s
              easy. Just click ‘Edit Text’ or double click me to add your own
              content and make changes to the font. Feel free to drag and drop
              me anywhere you like on your page.

              <br />
              <br />

              This is a great space to write a long text about your company and
              your services you can use this space to go into a little more
              detail about your company. Talk about your team and what services
              you provide. Tell your visitors the story of how you came up with
              the idea for your business and what makes you different from your
              competitors
            </p>
          </div>
          <div class="commercial-pic"></div>
        </div>

        <div class="pic-card-2">
          <div class="infrastructure-pic"></div>
          <div class="card infrastructure-text">
            <div class="litlle-line"></div>
            <h3>Infrastructure</h3>
            <p>
              I’m a paragraph. Click here to add your own text and edit me. It’s
              easy. Just click ‘Edit Text’ or double click me to add your own
              content and make changes to the font. Feel free to drag and drop
              me anywhere you like on your page.

              <br />
              <br />

              This is a great space to write a long text about your company and
              your services you can use this space to go into a little more
              detail about your company. Talk about your team and what services
              you provide. Tell your visitors the story of how you came up with
              the idea for your business and what makes you different from your
              competitors
            </p>
          </div>
        </div>
        <div class="pic-card-3">
          <div class="residential-text">
            <div class="litlle-line"></div>
            <h3>Residential</h3>
            <div class="residential-pic-2"></div>
            <p>
              I’m a paragraph. Click here to add your own text and edit me. It’s
              easy. Just click ‘Edit Text’ or double click me to add your own
              content and make changes to the font. Talk about your team and
              what services you provide. Tell your visitors the story of how you
              came up with the idea for your business and what makes you
              different from your competitors
            </p>
          </div>

          <div class="residential-pic"></div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* ///////////////////////////////// */
/* This is the KEY part - make it cover the screen! */
.hero {
  margin-top: -4.9rem;
  position: relative; /* Needed for absolute positioning of video and content */
  width: 100%;
  height: 100vh; /* Use viewport height to fill the screen */
  overflow: hidden; /* Hide any overflow from the video */
  /* ////////////////////////////////// */
  background-size: cover;
  background-position: center;
  position: sticky;
  top: -100px;
  z-index: 1;
}

.hero-video {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  object-fit: cover; /* Crucial:  Makes the video fill the container */
  z-index: 0; /* Keep the video behind the content */
}

.hero-content {
  position: relative;
  top: 10rem;
  /* height: 100vh; */
  z-index: 2; /* Bring the text to the front */
  color: white; /* Adjust text color as needed */
  text-align: center; /* Center the text */
  padding: 20px; /* Add some padding */
  display: flex; /* Enable Flexbox */
  flex-direction: column; /* Stack items vertically */
  justify-content: center; /* Vertically center content */
  align-items: center; /* Horizontally center content */
}

h1 {
  font-size: 3.5em;
  margin-bottom: 10px;
}

p {
  font-family: "Times New Roman", Times, serif;
  font-size: 1.2rem;
  font-weight: 100;
  max-width: 700px;
  margin: auto;
  text-align: center;
}

.hero-text-1 {
  padding-top: 0.5rem;
}

.hero-learn-btn {
  margin-top: 4rem;
  width: 200px;
  height: 50px;
  border-radius: 15px;
  background-color: transparent;
  border: 1.5px #d8d300 solid;
  color: white;
  font-size: 23px;
  font-family: "Times New Roman", Times, serif;
  font-weight: lighter;
  letter-spacing: 1px;
}

/* /////////////////////////// */
.container {
  min-height: 180vh; /* Adjust as needed */
}

.content-section {
  padding: 20px;
  position: relative;
  z-index: 2;
  background-color: #f0f0f0;
  height: 100%;
  padding-bottom: 5rem;
}

/* ///////////////////////////////////////////////// */
.service-texts {
  display: flex;
  margin-top: 3rem;
  padding: 0 4rem;
}

.service-text-1 {
  max-width: 600px;
}
.service-text-1 h2 {
  font-size: 3rem;
  font-weight: 500;
  line-height: 50px;
  color: #d8d300;
  text-align: left;
}

.service-p1 {
  margin-bottom: 1rem;
  font-weight: 300;
  font-size: 30px;
  text-align: left;
}

.service-text-2 {
  max-width: 500px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: auto;
}

.services-btn button {
  padding: 1rem 2rem;
  border-radius: 10px;
  border: none;
  background-color: #d8d300;
  margin-right: -20rem;
}

.card {
  text-align: left;
}

/* ////////////////////////////////////////////////////////////// */
.pic-card-1 {
  display: flex;
  margin-top: 5rem;
}
.pic-card-1 p {
  text-align: left;
}
.pic-card-1 h3 {
  padding-bottom: 0.5rem;
}

.litlle-line {
  border-top: 2px solid black;
  width: 60px;
  padding-bottom: 0.5rem;
}

.commercial-text {
  width: 50%;
  background-color: #d8d300;
  padding: 2rem;
  height: 320px;
}

/* ////////////////////////////////////////////////////////// */
.commercial-pic {
  background-image: url(../assets/wwd-3.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  height: 650px;
  width: 50%;
  margin-top: -4rem;
  border-radius: 30px 0px 0px 30px;
}

/* /////////////////////////////////////////// */
.pic-card-2 {
  display: flex;
  margin-top: 10rem;
}

.pic-card-2 p {
  text-align: left;
}

.pic-card-2 h3 {
  padding-bottom: 0.5rem;
}

.infrastructure-text {
  width: 50%;
  background-color: #d8d300;
  padding: 2rem;
  height: 320px;
}

.infrastructure-pic {
  background-image: url(../assets/wwd-2.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  height: 650px;
  width: 50%;
  margin-top: -10rem;
  border-radius: 0px 30px 30px 0px;
}

/* /////////////////////////////////////// */
.pic-card-3 {
  display: flex;
  margin-top: 10rem;
}
.pic-card-3 p {
  text-align: left;
}

.pic-card-3 h3 {
  padding-bottom: 0.5rem;
}

.residential-text {
  padding-left: 2rem;
  padding-right: 2rem;
  display: flex;
  flex-direction: column;
  text-align: left;
  gap: 1rem;
  width: 50%;
  background-color: #d8d300;
  height: 650px;
  border-radius: 0px 30px 30px 0px;
}
.residential-text .litlle-line {
  margin-top: 2rem;
  margin-bottom: -1rem;
}

.residential-pic {
  background-image: url(../assets/wwd-1.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  height: 650px;
  width: 50%;
  border-radius: 30px 30px 30px 30px;
}

.residential-pic-2 {
  background-image: url(../assets/wwd-4.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  height: 300px;
  width: 100%;
  border-radius: 30px 30px 30px 30px;
}
</style>
