<template>
  <div class="header">
    <TheHeader />
  </div>
  <div class="arrow">
    <h1><RouterLink :to="`/`">&#8592; Back to home page</RouterLink></h1>
  </div>
  <div class="theText">
    <h2>This project was created by Richard Retter</h2>
    <p>
      I wanted to do so much more for this project but sadly because of family issues this is all I
      had time for. I will continue working on this site and I will update the github repository
      with further updates.
    </p>
  </div>
  <div class="detailsList">
    <h3>Here are my contact details in case you would like to get in touch with me:</h3>
    <ul>
      <li>Name: Richard Retter</li>
      <li>Address: 22848 Norederstedt Ochsenzoller Straße 182</li>
      <li>E-mail: retterrichard55@gmail.com</li>
      <li>Phone Number: +49 152 37726568</li>
    </ul>
  </div>
  <div class="note">
    <p>This was a project for the Full Stack Web Developer course from Hamburg Coding School</p>
  </div>
</template>

<script>
import TheHeader from '../components/TheHeader.vue';
export default {
  components: {
    TheHeader
  }
};
</script>

<style scoped>
.note {
  text-align: center;
}
.detailsList {
  text-align: center;
}
ul {
  list-style-type: none;
}
.theText {
  text-align: center;
  margin: 70px 70px;
}
a {
  text-decoration: none;
  color: white;
}
.header {
  height: 80px;
  width: 100vw;
  display: flex;
  margin: 0 auto;
  border-bottom: 3px solid white;
  border-top: 3px solid white;
}
</style>
