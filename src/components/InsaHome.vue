<template>
  <v-container class="main-page">
    <v-alert title="ANUNCIO IMPORTANTE" text="..." type="error">
      <div class="announcement-container">
        <div class="festival-announcement">
          <v-img src="https://d1ro9wdeur3r20.cloudfront.net/photos/festival_verano_2023.jpg" />
        </div>
        <div class="video-festival-container">
          <video controls>
            <source
              src="https://d1ro9wdeur3r20.cloudfront.net/photos/festival_verano_2023.mp4"
              type="video/mp4"
            />
          </video>
        </div>
      </div>
    </v-alert>
    <div class="cover-image">
      <img class="img1" src="https://d1ro9wdeur3r20.cloudfront.net/photos/cover_page_kids.jpg" />
    </div>
    <!-- ABOUT US SECTION -->
    <v-container id="about" class="about-us-section">
      <v-row>
        <v-col cols="12" sm="12" xs="12" lg="6" xl="6">
          <v-card flat class="card-about">
            <v-card-title class="display-1">{{ $t("about") }}</v-card-title>
            <v-card-text class="body-2 text-about">
              <p class="text-justify">{{ $t("content-insa.about[0]") }}</p>
              <p class="text-justify">{{ $t("content-insa.about[1]") }}</p>
              <p class="text-justify">{{ $t("content-insa.about[2]") }}</p>
              <p class="text-justify">{{ $t("content-insa.about[3]") }}</p>
              <p class="text-right">{{ $t("content-insa.about[4]") }}</p>
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" sm="12" xs="12" lg="6" xl="6" class="about-us-image-container">
          <v-img
            class="main-page-school"
            src="https://d1ro9wdeur3r20.cloudfront.net/photos/main_page_school.png"
          >
          </v-img>
        </v-col>
      </v-row>
    </v-container>
    <!-- EDUCATIONAL PROJECT SECTION -->
    <v-container id="project" class="project-section">
      <v-row>
        <v-col cols="12" sm="12" xs="12" lg="12" xl="12">
          <v-img class="tree-right" src="../assets/tree_right.png"></v-img>
        </v-col>
        <v-col cols="12" sm="12" xs="12" lg="12" xl="12" align="center">
          <v-card flat class="card-about2">
            <v-card-title class="display-1 content-project">
              {{ $t("content-insa.about[5]") }}
            </v-card-title>
            <v-card-text class="body-2">
              <p class="text-center">{{ $t("content-insa.about[6]") }}</p>
              <p class="text-center">{{ $t("content-insa.about[7]") }}</p>
              <p class="text-center">{{ $t("content-insa.about[8]") }}</p>
              <p class="text-center">{{ $t("content-insa.about[9]") }}</p>
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" sm="12" xs="12" lg="12" xl="12">
          <v-img class="tree-left" src="../assets/tree_left.png"></v-img>
        </v-col>
      </v-row>
    </v-container>
    <!-- HISTORY SECTION -->
    <v-container id="history" class="history-section">
      <v-row align="center">
        <v-col cols="12" sm="12" xs="12" lg="6" xl="6" align="right">
          <div class="history-image">
            <v-img
              class="img2"
              src="https://d1ro9wdeur3r20.cloudfront.net/photos/school_life_1.jpg"
            >
            </v-img>
          </div>
        </v-col>
        <v-col cols="12" sm="12" xs="12" lg="6" xl="6" align="center" justify="center">
          <v-card flat class="card-history">
            <v-card-title class="display-1">{{ $t("history") }}</v-card-title>
            <v-card-text class="body-2">
              <p class="text-left">{{ $t("content-insa.history") }}</p>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
    <!-- MISSION SECTION -->
    <v-container id="mission" class="mission-section">
      <v-row align="center">
        <v-col cols="12" sm="12" xs="12" lg="6" xl="6">
          <v-card flat class="card-mission">
            <v-card-title class="display-1">{{ $t("mission") }}</v-card-title>
            <v-card-text class="body-2">
              <p class="text-left">{{ $t("content-insa.mission") }}</p>
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" sm="12" xs="12" lg="6" xl="6">
          <div class="mission-image">
            <v-img src="https://d1ro9wdeur3r20.cloudfront.net/photos/main_page_mission.png">
            </v-img>
          </div>
        </v-col>
      </v-row>
    </v-container>
    <v-container id="vision" class="vision-section">
      <v-row align="center">
        <v-col cols="12" sm="12" xs="12" lg="6" xl="6" align="right">
          <div class="vision-image">
            <v-img src="https://d1ro9wdeur3r20.cloudfront.net/photos/main_page_vision.png"></v-img>
          </div>
        </v-col>
        <v-col cols="12" sm="12" xs="12" lg="6 " xl="6">
          <v-card flat class="card-vision">
            <v-card-title class="display-1">{{ $t("vision") }}</v-card-title>
            <v-card-text class="body-2">
              <p class="text-left">{{ $t("content-insa.vision") }}</p>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-container>
</template>
<script lang="ts">
import Vue from "vue";

const InsaHome = Vue.extend({
  name: "InsaHome",
});
export default InsaHome;
</script>

<style lang="scss" scoped>
@import "../styles/settings.scss";

.main-page {
  width: 100% !important;
  max-width: 100% !important;
  height: 100% !important;
  padding: 0px !important;
  .announcement-container {
    display: flex;
    justify-content: center;
    align-items: center;
    .video-festival-container video {
      padding-left: 20px;
      object-fit: cover;
    }
    .festival-announcement {
      max-width: 100%;
      max-height: 100%;
      width: 500px;
      height: 100%;
      border-radius: 10px; /* Adjust the value as needed */
      border: 2px solid #ccc;
    }
  }
  .cover-image {
    width: 100%;
    background-color: white;
    .img1 {
      width: inherit;
      mask-size: cover;
      mask-position: left bottom;
      mask-repeat: no-repeat;
    }
  }
  .about-us-section {
    padding-top: 5%;
    padding-bottom: 15%;
    max-width: 1400px;
    .card-about {
      .display-1 {
        font-family: "Montserrat", sans-serif !important;
      }
      .body-2 {
        font-family: "Montserrat", sans-serif !important;
      }
      .text-about {
        font-style: normal;
        font-weight: normal;
        line-height: 160%;
        color: black;
      }
    }
    .about-us-image-container {
      .main-page-school {
        max-width: 816px;
        max-height: 507px;
      }
    }
  }
  .project-section {
    background-color: #f5f5f5;
    margin: 0px;
    padding: 0px;
    max-width: 100% !important;
    .tree-right {
      position: relative;
      float: right;
      max-width: 60%;
      top: -45%;
    }
    .tree-left {
      position: relative;
      float: left;
      max-width: 60%;
      bottom: -45%;
    }
    .card-about2 {
      .display-1 {
        font-family: "Montserrat", sans-serif !important;
        color: black;
      }
      .body-2 {
        font-family: "Montserrat", sans-serif !important;
        color: black;
      }
      background-color: #f5f5f5;
      max-width: 1104px;
      .content-project {
        justify-content: center;
      }
    }
  }
  .history-section {
    padding-top: 20%;
    padding-bottom: 20%;
    max-width: 1268px;
    .history-image {
      max-width: 672px;
      max-height: 519px;
    }
    .card-history {
      .display-1 {
        font-family: "Montserrat", sans-serif !important;
        color: black;
      }
      .body-2 {
        font-family: "Montserrat", sans-serif !important;
        color: black;
      }
      max-width: 672px;
    }
  }
  .mission-section {
    max-width: 1372px;
    .card-mission {
      .display-1 {
        font-family: "Montserrat", sans-serif !important;
        color: black;
      }
      .body-2 {
        font-family: "Montserrat", sans-serif !important;
        color: black;
      }
      top: 20%;
      max-width: 672px;
    }
    .mission-image {
      max-width: 960px;
      max-height: 482px;
      padding: 5%;
    }
  }
  .vision-section {
    padding-top: 10%;
    padding-bottom: 10%;
    .card-vision {
      width: 100%;
      .display-1 {
        font-family: "Montserrat", sans-serif !important;
        color: black;
      }
      .body-2 {
        font-family: "Montserrat", sans-serif !important;
        color: black;
      }
    }
    .vision-image {
      max-width: 542px;
      max-height: 447px;
      padding: 5%;
    }
  }
}
</style>
