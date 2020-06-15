<template>
  <div class="jobItem">
    <div class="job_top_info">
      <div class="year">{{ year }}</div>
      <div class="title">{{ title }}</div>
    </div>
    <div class="logo">
      <img class="jobImage" :src="require('@/assets/jobImages/' + logo + '')" />
    </div>
    <div class="employer">{{ employer }}</div>
  </div>
</template>

<script>
export default {
  name: "JobItem",
  props: {
    year: String,
    title: String,
    logo: String,
    employer: String,
  },
};
</script>

<style>
.jobItem {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100%;
  width: 100px;
  margin: 10px 13px;
}

.job_top_info {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 51px;
}

.title {
  font-size: 12px;
  font-weight: 600;
}
.year {
  font-weight: normal;
  font-size: 12px;
}

.jobImage {
  height: 70px;
  width: 70px;
  border-radius: 50%;
  border: 2px solid #2c3e50;
  background-color: white;
  margin: 10px 0;
}

.employer {
  font-size: 12px;
  height: 51px;
  font-weight: normal;
}

@media screen and (max-width: 1800px) and (min-width: 1300px) {
  .title {
    font-size: 10px;
  }
}
</style>
