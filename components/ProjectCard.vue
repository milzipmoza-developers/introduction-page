<template>
  <div
    class="project-card"
  >
    <div class="card-content">
      <div v-if="logoOutLine" class="card-logo outline">
        <img :width="width" :height="height" :src="logoSrc" style="border-radius: 20px"/>
      </div>
      <div v-if="!logoOutLine" class="card-logo nooutline">
        <img :width="width" :height="height" :src="logoSrc" style="border-radius: 20px"/>
      </div>
      <div class="card-text">
        <div class="card-title">
          {{ title }}
        </div>
        <div class="card-description">
          <span v-for="(line, i) in contentLines" v-bind:key="i">{{ line }}<br></span>
        </div>
        <div>
          <icon-button
            :href="githubHref"
            icon="fab fa-github"
            color="#FFFFFF"
          ></icon-button>
          <image-button
            v-if="useImgBtn"
            :href="imgBtnHref"
          ></image-button>
          <v-btn
            class="card-btn"
            text
            color="white accent-4"
            :to="descPage"
          >
            더 알아보기
          </v-btn>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import IconButton from "../components/IconButton.vue"
  import ImageButton from "../components/ImageButton"

  export default {
    name: "ProjectCard.vue",
    props: {
      logoOutLine: {
        type: Boolean
      },
      width: {
        type: String
      },
      height: {
        type: String
      },
      logoSrc: {
        type: String
      },
      title: {
        type: String
      },
      contentLines: {
        type: Array
      },
      githubHref: {
        type: String
      },
      descPage: {
        type: String
      },
      useImgBtn: {
        type: Boolean
      },
      imgBtnHref: {
        type: String,
      }
    },

    components: {
      IconButton,
      ImageButton
    }
  }
</script>

<style scoped>
  /* card */
  .project-card {
    background-color: black !important;
    border: 1px solid white !important;
    padding: 16px;
    margin-top: 12px;
    margin-bottom: 36px;
    border-radius: 15px;
  }

  .project-card::after {
    content: " ";
    display: block;
    height: 0;
    clear: both;
  }

  .card-logo {
    margin: 16px;
  }

  .outline {
    float: left;
    border: 1px solid white;
    border-radius: 20px;
  }

  .nooutline {
    float: left;
  }

  .card-title {
    color: white;
    font-size: 32px;
    font-weight: bold;
    padding-bottom: 12px;
  }

  .card-btn {
    background-color: white;
    margin-right: 4px;
    float: right;
  }

  .card-description {
    color: white;
    font-size: 16px;
    padding-bottom: 16px;
  }

  .card-text {
    padding-bottom: 16px;
  }
</style>
