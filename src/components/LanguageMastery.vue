<template>
  <div class="mastery">
    <div class="bubble">{{ name }}</div>
    <div class="bar">
      <div class="outside">
        <div class="inside" :style="{ width: experience + '%' }" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "LanguageMastery",
  props: {
    name: String,
    experience: Number,
  },
};
</script>

<style>
.mastery {
  width: 100%;
  display: flex;
  justify-content: space-between;
}

.bar {
  width: 195px;
  padding: 5px;
  padding-left: 20px;
}

.outside {
  width: 100%;
  height: 100%;
  background: #f5f5f5;
  border-radius: 2px;
}

.inside {
  height: 100%;
  background: linear-gradient(90deg, #5dc2fb 0%, #5df1fb 99.83%);
  border-radius: 2px;
}

@media screen and (max-width: 420px) {
  .bar {
    width: 45vw;
  }
}
</style>
