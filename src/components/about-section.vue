<template>
  <section id="about" class="about">
    <h2>Learn About Us</h2>
    <p class="abt-p1">
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tenetur sapiente
      dolore temporibus?
    </p>

    <div class="about-cards">
      <div class="card card-1">
        <h3>We Buy</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio in
          placeat esse natus consequuntur dolores.
        </p>
      </div>
      <div class="card card-2">
        <h3>We Build</h3>
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio in
          placeat esse natus consequuntur dolores.
        </p>
      </div>
      <div class="card card-3">
        <a href="#">
          <h3>We Sell</h3>
          <p>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Optio in
            placeat esse natus consequuntur dolores.
          </p>
        </a>
      </div>
    </div>

    <div class="about-text-pic">
      <div class="about-text">
        <h2>About Our Company</h2>
        <p class="abt-company-p1">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Harum minus
          molestias reiciendis qui fugit quo est aliquid, saepe explicabo et
          placeat perferendis natus veniam? Lorem ipsum dolor sit amet
          consectetur, adipisicing elit. Dolor, saepe consectetur.
        </p>

        <div class="signature">
          <div class="sign-img-container">
            <div class="img-signature"></div>
          </div>
          <h3>Okeowo Michael</h3>
          <p>Web Developer</p>
        </div>
      </div>

      <div class="about-circle-pic">
        <!-- <img src="" alt="" /> -->
      </div>
    </div>

    <div class="county">
      <div class="count year">
        <h3>1968</h3>
        <p>Year of Establishment</p>
      </div>
      <div class="divide-line"></div>
      <div class="count line projects">
        <h3>282</h3>
        <p>Projects Completed</p>
      </div>
      <div class="divide-line"></div>
      <div class="count line employees">
        <h3>150</h3>
        <p>Professional Employees</p>
      </div>
      <div class="divide-line"></div>
      <div class="count line partners">
        <h3>35</h3>
        <p>Business Partners</p>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about {
  margin-top: 4rem;
  padding: 1rem 1rem;
  background-color: #f5f5f5; /* Light background for contrast */
  padding-bottom: 5rem;
  padding-top: 3rem;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

a {
  text-decoration: none;
  color: black;
}

h2 {
  font-size: 3rem;
  font-weight: 500;
  line-height: 50px;
  color: #d8d300;
}

.abt-p1 {
  padding-top: 1rem;
  font-size: 1.2rem;
  max-width: 550px;
  margin: auto;
  font-weight: 100;
}

h3 {
  /* display: flex;
    justify-content: center; */
  font-size: 2rem;
  text-align: center;
}

p {
  text-align: center;
  line-height: 1;
}

/* ////////////////////// */
.about-cards {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin-top: 3.5rem;
  padding-bottom: 4rem;
}

.card {
  max-width: 350px;
  height: auto;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border: 1.5px solid #d8d300;
  border-radius: 5px;
  padding: 3rem 1rem;
}

.card h3 {
  padding-bottom: 1rem;
}

/* /////////////////////////////////////////// */
.about-text-pic {
  margin-top: 6rem;
  display: flex;
}

.about-text {
  max-width: 60%;
  padding-left: 2rem;
  text-align: left;
}
.about-text p {
  text-align: left;
}
.about-text h2 {
  text-align: left;
}

.abt-company-p1 {
  padding-top: 1rem;
  line-height: 20px;
  max-width: 650px;
}

.signature {
  display: flex;
  flex-direction: column;
  margin-top: 4rem;
  /* text-align: left; */
}
.img-signature {
  background-image: url(../assets/signature.png);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  height: 70px;
  width: 300px;
  margin-left: -1.5rem;
}

.sign-img-container {
  display: flex;
  justify-content: left;
  align-items: center;
}

.signature h3 {
  text-align: left;
  margin-bottom: -8px;
  margin-top: -0.2rem;
}
.signature p {
  text-align: left;
  padding-left: 4rem;
  padding-top: 0.5rem;
}

/* /////////////////////// */
.about-circle-pic {
  background-image: url(../assets/team-2.jpeg);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  height: 450px;
  width: 450px;
  position: right;
  margin: auto;
  border-radius: 50%;
  /* z-index: 100; */
}

/* ////////////////////////////////// */
.county {
  background-color: #d8d300;
  color: #f5f5f5;
  height: 150px;
  margin-top: 3rem;
  display: flex;
  justify-content: center;
  /* gap: 15rem; */
}

.count {
  max-width: 350px;
  height: 100px;
  font-size: 2rem;
  font-weight: 700;
  line-height: 60px;
  padding-left: 5rem;
  padding-right: 5rem;
  padding-top: 2rem;
}
.count h3 {
  margin: auto;
  padding: auto;
  font-size: 3.5rem;
}
.count p {
  font-size: 14px;
  max-width: 300px;
  padding-top: 5px;
}

.divide-line {
  border-left: 3px solid white;
  height: 65px;
  margin: auto 0;
}

/* .line {
    border-left: 3px solid white;
    height: 50px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-top: 3rem;
    margin: auto;
  } */
</style>
