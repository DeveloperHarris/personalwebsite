<template>
  <div class="mobileJobItem">
    <div class="mobileLogo">
      <img class="mobileJobImage" :src="require('@/assets/jobImages/' + logo + '')" />
      <div class="mobileEmployer">{{employer}}</div>
      <div class="mobileTitle">{{title}}</div>
      <div class="jobRange">{{startDate}} - {{endDate}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MobileJobItem",
  props: {
    startDate: String,
    endDate: String,
    title: String,
    logo: String,
    employer: String
  }
};
</script>

<style>
.mobileJobItem {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 15px 0;
}

.mobileJobImage {
  height: 100px;
  width: 100px;
  border-radius: 50%;
  border: 2px solid #2c3e50;
  background-color: white;
  margin: 10px 0;
}

.mobileEmployer {
  font-size: 22px;
  font-weight: 600;
  height: 100%;
}

.mobileTitle {
  font-size: 22px;
  font-weight: normal;
  height: 100%;
}

.jobRange {
  font-style: italic;
  font-weight: 300;
  font-size: 22px;
}
</style>