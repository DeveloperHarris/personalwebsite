<template>
  <div class="profile_summary">
    <div class="profile_top_section">
      <div class="profile_photo"></div>
      <div class="name_title">
        <div class="name">Harris Rothaermel</div>
        <div class="title">CS Undergrad @ BYU</div>
      </div>
      <div class="location">
        <i class="fas fa-map-marker-alt"></i>
        Provo, UT
      </div>
      <div class="social">
        <a href="mailto:harris.rothaermel@gmail.com" target="_blank">
          <i class="fas fa-envelope fa-2x"></i>
        </a>
        <a href="https://www.linkedin.com/in/harrisrothaermel/" target="_blank">
          <i class="fab fa-linkedin fa-2x"></i>
        </a>
        <a href="https://github.com/DeveloperHarris" target="_blank">
          <i class="fab fa-github fa-2x"></i>
        </a>
        <a href="https://twitter.com/DeveloperHarris" target="_blank">
          <i class="fab fa-twitter fa-2x"></i>
        </a>
      </div>
    </div>
    <div class="divider"></div>
    <div class="profile_bottom_section">
      <div class="skills_title">Tech Stack</div>
      <div class="programming_languages">
        <LangaugeMastery
          v-for="language in languages"
          :key="language.name"
          :name="language.name"
          :experience="language.experience"
          class="language"
        />
      </div>
      <div class="skills">
        <div class="fullstack">
          <div class="skill_header">Fullstack Development:</div>&nbsp;React, Vue, Express, Node, Django, MongoDB, SQL, AWS, Firebase, Unix, Git, CT/CI
        </div>
        <div class="game_dev">
          <div class="skill_header">Game Development:</div>&nbsp;Unreal Engine, Unity, Virtual & Augmented Reality, World Machine
        </div>
      </div>
      <div class="engineering">
        <div class="skill_header">Mechanical & EE:</div>&nbsp;PCB Design (EAGLE), HAM Radio (KJ7NFC), 3D CAD (Solidworks & Fusion 360), Additive Manufacturing (3D Printing), Laser & Plasma Cutting, Welding, Soldering
      </div>
      <div class="general">
        <div class="skill_header">General:</div>&nbsp;Adobe Software Suite, Microsoft Office, Figma
      </div>
    </div>
  </div>
</template>

<script>
import LangaugeMastery from "./LanguageMastery.vue";

export default {
  name: "ProfileSummary",
  components: {
    LangaugeMastery
  },
  data() {
    return {
      languages: [
        { name: "C++", experience: 70 },
        { name: "Java", experience: 60 },
        { name: "Javascript", experience: 50 },
        { name: "Python", experience: 45 }
      ]
    };
  }
};
</script>

<style>
.profile_summary {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: start;

  width: 330px; /* 75vw seems good for mobile */
  height: 100%;

  position: relative;
  top: -15vh;

  padding-bottom: 5px;

  background: #ffffff;
  box-shadow: 0px 4px 25px rgba(0, 0, 0, 0.25);
}

.profile_top_section {
  height: 325px;

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: space-evenly;

  position: relative;
  top: -7vh;
  margin-bottom: -7vh;

  width: 75%;
}

.profile_photo {
  width: 150px;
  height: 150px;

  background: url(../assets/headshot.jpeg);
  background-size: 100%;
  border: 4px solid #ffffff;
  border-radius: 144px;
}

.name_title,
.location,
.social {
  padding: 5px 0;
}

.name {
  font-weight: 700;
  font-size: 20px;
}

.title {
  font-size: 16px;
}

.social {
  width: 75%;
  display: flex;
  justify-content: space-between;
}

.social a {
  text-decoration: none;
  color: #2c3e50;
}

.divider {
  width: 100%;
  border-bottom: 1px solid #c2c2c2;
  margin: 10px 0;
}

.profile_bottom_section {
  width: 90%;
  display: flex;
  flex-direction: column;
  align-items: start;
  margin: 0 auto;
}

.skills_title {
  font-weight: 700;
  font-size: 20px;
}

.programming_languages {
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
}

.language {
  margin-top: 10px;
}

.skills {
  margin-top: 10px;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: start;
}

.fullstack,
.game_dev,
.engineering,
.general {
  margin-top: 10px;
  text-align: left;
  font-size: 14px;
  font-weight: 300;
}

.skill_header {
  display: inline;
  font-weight: 400;
  text-decoration: underline;
}
</style>