<template>
  <div class="portfolioItem" v-on:click="showModal">
    <div class="portfolioImageContainer">
      <img
        class="portfolioImage"
        :src="require('@/assets/portfolioImages/' + image + '')"
      />
    </div>
    <div class="portfolioItemTitle">{{ title }}</div>
    <modal
      class="modal"
      :name="title"
      :width="modalWidth"
      height="auto"
      :scrollable="true"
    >
      <div class="modal_title">{{ title }}</div>
      <div class="modal_content">
        <VueMarkdown :source="story"></VueMarkdown>
      </div>
    </modal>
  </div>
</template>

<script>
import VueMarkdown from "vue-markdown";

export default {
  name: "PortfolioItem",
  props: {
    title: String,
    image: String,
    story: String,
  },
  components: {
    VueMarkdown,
  },
  data() {
    return {
      modal: false,
    };
  },
  methods: {
    showModal() {
      this.$modal.show(this.title);
    },
  },
  computed: {
    modalWidth: function() {
      return window.innerWidth <= 700 ? "80%" : "50%";
    },
  },
};
</script>

<style>
.portfolioItem {
  margin-bottom: 15px;
  cursor: pointer;
}

.portfolioImageContainer {
  width: 400px;
  height: 225px;
}

.portfolioImage {
  object-fit: cover;
  height: 100%;
  width: 100%;
  box-shadow: 0px 4px 25px rgba(0, 0, 0, 0.25);
  margin-bottom: 5px;
}

.portfolioItemTitle {
  font-weight: 600;
  text-align: left;
  font-size: 22px;
}

.modal_title {
  font-size: 30px;
  font-weight: 600;
  margin: 10px 10px;
}

.modal_content {
  margin: 20px;
}

@media screen and (min-width: 421px) and (max-width: 1200px) {
  .portfolioImageContainer {
    width: 300px;
    height: 169px;
  }
}

@media screen and (max-width: 420px) {
  .portfolioImageContainer {
    width: 100%;
  }

  .modal_title {
    font-size: 24px;
  }
}
</style>
