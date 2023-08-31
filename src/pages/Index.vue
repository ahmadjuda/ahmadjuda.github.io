<template>
  <div>
    <div class="page-header clear-filter" filter-color="orange">
      <parallax
        class="page-header-image"
        style="background-image:url('img/bg_se.jpg')"
      >
      </parallax>
      <div class="container">
        <div class="photo-container">
          <img src="img/juy.jpeg" alt="" />
        </div>
        <h3 class="title">Ahmad Juda Prasetia</h3>
        <p class="category">Software Engineer</p>
      </div>
    </div>
    <div class="section">
      <div class="container">
        <div class="button-container">
          <a
            href="https://www.linkedin.com/in/ahmad-juda-prasetia-340820179/"
            class="btn btn-primary btn-round btn-lg btn-icon"
            rel="tooltip"
            title="Let's connect on LinkedIn"
            target="_blank"
          >
            <i class="fab fa-linkedin"></i>
          </a>
          <a
            href="https://www.instagram.com/ahmadjuda/"
            class="btn btn-primary btn-round btn-lg btn-icon"
            rel="tooltip"
            title="Follow me on Instagram"
            target="_blank"
          >
            <i class="fab fa-instagram"></i>
          </a>
        </div>
        <h3 class="title">About me</h3>
        <h5 class="description">
          I'm a Software Engineer and i have experience more than 3 years in software development. Experienced with a skill in Vue.js, SQL, and Laravel. I am currently working as a software engineer at Soca AI. Below I attached my work experience as follows.
        </h5>
        <div class="row">
          <div class="col-md-6 ml-auto mr-auto">
            <h4 class="title text-center">My Portfolio</h4>
          </div>
          <tabs
            pills
            class="w-100 nav-align-center"
            tab-content-classes="gallery"
            tab-nav-classes="nav-pills-just-icons"
            type="primary"
          >
            <tab-pane title="Website">
              <i slot="label" class="now-ui-icons"><p class="mb-0" style="font-size: 20px; padding-top: 20px;">Website</p></i>

              <div class="col-md-12 ml-auto mr-auto">
                <div class="row collections">
                  <div class="col-md-6" v-for="(value, index) in data" :key="index">
                    <div class="card" style="border-radius: 15px;">
                      <el-carousel style="border-top-left-radius: 15px; border-top-right-radius: 15px;">
                        <el-carousel-item v-for="(img, i) in value.images" :key="i">
                          <img class="d-block" :src="img.src" :alt="img.label" style="height: 100%;" />
                        </el-carousel-item>
                      </el-carousel>
                      <div class="card-body" style="-webkit-box-shadow: 0px -5px 20px 0px rgba(0, 0, 0, 0.3); box-shadow: 0px -5px 20px 0px rgba(0, 0, 0, 0.3); border-bottom-left-radius: 15px; border-bottom-right-radius: 15px;">
                        <h5 class="font-weight-bolder">{{ value.name }}</h5>
                        <p>{{ value.desc }}</p>
                        <h6 class="font-weight-bolder">Technologies :</h6>
                        <p>{{ value.tech }}</p>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </tab-pane>

            <tab-pane title="Desktop">
              <i slot="label" class="now-ui-icons"><p class="mb-0" style="font-size: 20px; padding-top: 20px;">Desktop</p></i>

              <div class="col-md-12 ml-auto mr-auto">
                <div class="row collections">
                  <div class="col-md-6" v-for="(value, index) in data_desktop" :key="index">
                    <div class="card" style="border-radius: 15px;">
                      <el-carousel style="border-top-left-radius: 15px; border-top-right-radius: 15px;">
                        <el-carousel-item v-for="(img, i) in value.images" :key="i">
                          <img class="d-block" :src="img.src" :alt="img.label" style="height: 100%;" />
                        </el-carousel-item>
                      </el-carousel>
                      <div class="card-body" style="-webkit-box-shadow: 0px -5px 20px 0px rgba(0, 0, 0, 0.3); box-shadow: 0px -5px 20px 0px rgba(0, 0, 0, 0.3); border-bottom-left-radius: 15px; border-bottom-right-radius: 15px;">
                        <h5 class="font-weight-bolder">{{ value.name }}</h5>
                        <p>{{ value.desc }}</p>
                        <h6 class="font-weight-bolder">Technologies :</h6>
                        <p>{{ value.tech }}</p>
                      </div>
                    </div>
                  </div>
                  <div class="col-md-6"></div>
                </div>
              </div>
            </tab-pane>
          </tabs>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { Tabs, TabPane } from '@/components';
import { Carousel, CarouselItem } from 'element-ui';

export default {
  name: 'profile',
  bodyClass: 'profile-page',
  components: {
    Tabs,
    TabPane,
    [Carousel.name]: Carousel,
    [CarouselItem.name]: CarouselItem
  },
  data() {
    return {
      data: [
        {
          name: "Soca Creator Mobile Web Application",
          desc: "SOCA is an AI platform built to accelerate & transform your business. Create your content freely and make it more interesting.",
          tech: "Vue Js, Vuex",
          images: [
            {
              label: "Login",
              src: "img/portfolio/soca_creator_login.png"
            },
            {
              label: "Home",
              src: "img/portfolio/soca_creator_home.png"
            }
          ]
        },
        {
          name: "YKKBI - Seroja",
          desc: "SEROJA is an application used to provide general information regarding services provided by YKKBI for active and retired employees of Bank Indonesia.",
          tech: "Laravel, Vue Js, PostgreSQL, Firebase",
          images: [
            {
              label: "Login",
              src: "img/portfolio/seroja.png"
            }
          ]
        },
        {
          name: "YKKBI - DIGIBIKES",
          desc: "DIGIBIKES is an application used to provide general information regarding services provided by YKKBI for active Bank Indonesia employees.",
          tech: "Laravel, Vue Js, PostgreSQL, Firebase",
          images: [
            {
              label: "Login",
              src: "img/portfolio/digibikes.png"
            }
          ]
        },
        {
          name: "IAPI - Back Office",
          desc: "This application is used to manage various services such as certification, training, membership of the Indonesian Institute of Certified Public Accountants (IAPI).",
          tech: "Spring Boot, Vue Js, PostgreSQL, Socket.io",
          images: [
            {
              label: "Login",
              src: "img/portfolio/bo_iapi.png"
            }
          ]
        },
        {
          name: "IAPI - Front Office",
          desc: "This application is used to manage the entire certification and training process for Institute of Public Accountants (IAPI) members with a payment gateway using Midtrans, socket and Firebase for notifications.",
          tech: "Laravel, Vue Js, PostgreSQL, Socket.io, Firebase, Midtrans",
          images: [
            {
              label: "Login",
              src: "img/portfolio/fo_iapi.png"
            }
          ]
        },
        {
          name: "IAPI - LMS",
          desc: "Learning management system training free or paid for membership Institute of Public Accountant(IAPI) with payments gateway using Midtrans.",
          tech: "Laravel, Blade, PostgreSQL, Socket.io, Firebase, Midtrans",
          images: [
            {
              label: "Login",
              src: "img/portfolio/lms_iapi.png"
            }
          ]
        },
        {
          name: "IAPI - Grader",
          desc: "This application is used to manage question bank, question module, participant answer, announce result, is used by the Institute of Public Accountant(IAPI).",
          tech: "Laravel, Vue Js, PostgreSQL",
          images: [
            {
              label: "Login",
              src: "img/portfolio/grader_iapi.png"
            }
          ]
        },
        {
          name: "IAPI - Test Center",
          desc: "Test Centre CBT System for Public Accountants Certification Exam Back End And Front End, with synchronization between all of Test Centre in Indonesia and Grader System at the Central Institute of Public Accountant(IAPI).",
          tech: "Laravel, Vue Js, PostgreSQL",
          images: [
            {
              label: "Login",
              src: "img/portfolio/tc_iapi.jpeg"
            }
          ]
        },
      ],
      data_desktop: [
        {
          name: "KP3SKP - USKP Online",
          desc: "A desktop application that is used for online exam certification facilities for the tax consultant professional level.",
          tech: "Bootstrap, Vue Js, Vuex, Electron Js",
          images: [
            {
              label: "Login",
              src: "img/portfolio/exam_kp3skp.png"
            }
          ]
        },
      ]
    }
  }
};
</script>
<style>
.el-carousel__container {
  text-align: -webkit-center;
}
</style>
