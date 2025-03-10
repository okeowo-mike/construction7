<template>
  <footer id="footer" class="footer">
    <div class="horizontal-divider-line"></div>
    <div class="footer-container">
      <div class="part-1">
        <h3>OMO</h3>
        <P>Construction</P>
      </div>
      <div class="part-2">
        <div class="address">
          <h3>Head Office</h3>
          <p>500 Terry Francine Street, San Francisco, CA 94158</p>
        </div>
        <div class="socials">
          <h3>Socials</h3>
          <li><a href="#">FaceBook</a></li>
          <li><a href="#">Instagram</a></li>
          <li><a href="#">LinkedIn</a></li>
          <ul></ul>
        </div>
        <div class="enquire">
          <h3>Enquiries</h3>
          <p>For any inquiries, questions or commendations, please call: 123-456-7890</p>
        </div>
      </div>
      <div class="part-3">
        <div class="contact-btn">
          <button>Contact Us</button>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  margin-top: 4rem;
}

.horizontal-divider-line {
  border-top: 1.5px solid black;
  width: 90%;
  margin: 0 auto;
}

.footer-container {
  width: 100%;
  margin: 0 auto;
  margin-top: 1.5rem;
  display: grid;
  grid-template-columns: 1fr 3fr 1fr;
  justify-content: center;
  align-items: center;
}

/* ////////////////////////////////// */

h3 {
  font-size: 1.1rem;
  /* line-height: 10px; */
}
.part-1 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.part-1 h3 {
  font-size: 1.5rem;
}
.part-1 p {
  /* margin-top: -0.1rem; */
  font-size: smaller;
}

/* ///////////////////////////////////// */
.part-2 {
  display: flex; /* Enable Flexbox layout */
  flex-wrap: wrap; /* Allow items to wrap to the next line on smaller screens */
  justify-content: space-between; /* Distribute space evenly between the divs */
  padding: 20px; /* Add some padding around the container */
}

.part-2 > div {
  /* Style each of the direct child divs of part-2 */
  width: 30%; /* Occupy approximately one-third of the container width */
  margin-bottom: 20px; /* Add some space below each div */
}

/* Ensure h3 elements are aligned */
.part-2 h3 {
  margin-top: 0; /* Remove any default top margin from the h3 */
  margin-bottom: 10px; /* Add spacing between the h3 and the content below */
  font-size: 1.2rem; /* Adjust font size as needed */
}

/* Style the address div */
.address p {
  font-size: 0.9rem; /* Adjust font size as needed */
  line-height: 1.5; /* Improve readability */
}

/* Style the socials div */
.socials {
  list-style: none; /* Remove bullet points from the list */
  padding: 0; /* Remove default padding from the list */
}

.socials li {
  margin-bottom: 5px; /* Add spacing between list items */
}

.socials a {
  text-decoration: none; /* Remove underlines from links */
  color: #333; /* Set link color (adjust as needed) */
}

/* Style the enquiries div */
.enquire p {
  font-size: 0.9rem; /* Adjust font size as needed */
  line-height: 1.5; /* Improve readability */
}

/* Media query for smaller screens (adjust the breakpoint as needed) */
@media (max-width: 768px) {
  .part-2 > div {
    width: 100%; /* Take up the full width on smaller screens */
  }
}

/* ////////////////////////////////////////// */

.part-3 {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.contact-btn button {
  padding: 1rem 2rem;
  border-radius: 10px;
  border: none;
  background-color: #d8d300;
  /* margin-right: -10rem; */
}
</style>
