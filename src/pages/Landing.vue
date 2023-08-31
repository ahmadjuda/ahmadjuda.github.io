<template>
  <div>
    <div class="page-header clear-filter" filter-color="orange">
      <parallax
        class="page-header-image"
        style="background-image:url('img/bg5.jpg')"
      >
      </parallax>
      <div class="container">
        <div class="photo-container">
          <img src="img/ryan.jpg" alt="" />
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
          >
            <i class="fab fa-linkedin"></i>
          </a>
          <a
            href="https://www.instagram.com/ahmadjuda/"
            class="btn btn-primary btn-round btn-lg btn-icon"
            rel="tooltip"
            title="Follow me on Instagram"
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
            class="nav-align-center"
            tab-content-classes="gallery"
            tab-nav-classes="nav-pills-just-icons"
            type="primary"
          >
            <tab-pane title="Profile">
              <i slot="label" class="now-ui-icons"><h6>Website</h6></i>

              <div class="col-md-10 ml-auto mr-auto">
                <div class="row collections">
                  <div class="col-md-6">
                    <div class="card">
                      <el-carousel>
                        <el-carousel-item>
                          <img class="d-block" src="img/bg1.jpg" alt="First slide" />
                        </el-carousel-item>
                        <el-carousel-item>
                          <img class="d-block" src="img/bg3.jpg" alt="Second slide" />
                        </el-carousel-item>
                        <el-carousel-item>
                          <img class="d-block" src="img/bg4.jpg" alt="Third slide" />
                        </el-carousel-item>
                      </el-carousel>
                      <div class="card-body">
                        <h5 class="font-weight-bolder">Soca Creator Mobile Web Application</h5>
                        <p>SOCA is an AI platform built to accelerate & transform your business. Create your content freely and make it more interesting.</p>
                      </div>
                    </div>
                    <img src="img/bg11.jpg" alt="" class="img-raised" />
                  </div>
                  <div class="col-md-6">
                    <img src="img/bg7.jpg" alt="" class="img-raised" />
                    <img src="img/bg8.jpg" alt="" class="img-raised" />
                  </div>
                </div>
              </div>
            </tab-pane>

            <tab-pane title="Home">
              <i slot="label" class="now-ui-icons airplay"></i>

              <div class="col-md-10 ml-auto mr-auto">
                <div class="row collections">
                  <div class="col-md-6">
                    <img src="img/bg1.jpg" alt="" class="img-raised" />
                    <img src="img/bg3.jpg" alt="" class="img-raised" />
                  </div>
                  <div class="col-md-6">
                    <img src="img/bg8.jpg" alt="" class="img-raised" />
                    <img src="img/bg7.jpg" alt="" class="img-raised" />
                  </div>
                </div>
              </div>
            </tab-pane>

            <tab-pane title="Messages">
              <i slot="label" class="now-ui-icons sport_user-run"></i>

              <div class="col-md-10 ml-auto mr-auto">
                <div class="row collections">
                  <div class="col-md-6">
                    <img src="img/bg3.jpg" alt="" class="img-raised" />
                    <img src="img/bg8.jpg" alt="" class="img-raised" />
                  </div>
                  <div class="col-md-6">
                    <img src="img/bg7.jpg" alt="" class="img-raised" />
                    <img src="img/bg6.jpg" class="img-raised" />
                  </div>
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
  }
};
</script>
<style></style>
