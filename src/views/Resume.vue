<template>
  <div class="resume">
    <Hero />
    <div class="flexbox-top-content">
      <div class="flexbox-top-summary">
        <ProfileSummary />
      </div>
      <div class="flexbox-top-info">
        <div class="edu_title">Education</div>
        <Education />
        <div class="work_experience_title">Work Experience</div>
        <WorkExperience />
      </div>
    </div>
    <div class="flexbox-bottom-content">
      <div class="portfolio_title">Portfolio</div>
      <Portfolio />
    </div>
  </div>
</template>

<script>
import Hero from "../components/Hero.vue";
import ProfileSummary from "../components/ProfileSummary.vue";
import Education from "../components/Education.vue";
import WorkExperience from "../components/WorkExperience.vue";
import Portfolio from "../components/Portfolio.vue";

export default {
  name: "Resume",
  components: {
    Hero,
    ProfileSummary,
    Education,
    WorkExperience,
    Portfolio,
  },
};
</script>

<style>
.flexbox-top-content {
  width: 67.5%;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
}

.flexbox-bottom-content {
  width: 67.5%;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
}

.flexbox-top-summary {
  display: flex;
  justify-content: start;
  margin-bottom: -15vh;
}

.flexbox-top-info {
  display: flex;
  flex-direction: column;
  align-items: start;
  margin-left: 25px;
}

.edu_title,
.work_experience_title,
.portfolio_title {
  font-size: 28px;
  font-weight: 700;
}

.edu_title,
.work_experience_title,
.education,
.work_experience,
.portfolio_title {
  margin-top: 15px;
}

.portfolio_title {
  text-align: left;
  display: block;
}

.work_experience {
  flex-grow: 1;
}

@media screen and (max-width: 420px) {
  .flexbox-top-content,
  .flexbox-bottom-content {
    flex-direction: column;
    width: 85%;
    margin: 0 auto;
  }

  .flexbox-top-summary,
  .flexbox-top-info,
  .flexbox-bottom-content {
    align-items: center;
  }

  .flexbox-top-info {
    margin-left: 0;
  }
}

@media screen and (max-width: 800px) and (min-width: 421px) {
  .flexbox-top-content,
  .flexbox-bottom-content {
    width: 100%;
  }
}

@media screen and (min-width: 1921px) {
  .resume {
    width: 1920px;
    margin: 0 auto;
  }
}
</style>
