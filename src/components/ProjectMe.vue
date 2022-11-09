<template>
  <section class="section-banner section-shaped my-0 bg-color-1" id="project">
    <div class="container content-project">
      <div class="row justify-content-center">
        <div class="col-12 m-auto content-skill">
          <div class="content-skill-logo float-left text-white text-bold">
            <h2>My <span>Project</span></h2>
            <h6>Website and Design</h6>
          </div>
          <div class="container">
            <div class="row">
              <div class="col-sm-12">
                <swiper
                  :effect="'coverflow'"
                  :grabCursor="true"
                  :centeredSlides="true"
                  :slidesPerView="'auto'"
                  :autoplay="{
                    delay: 2500,
                    disableOnInteraction: false,
                  }"
                  :coverflowEffect="{
                    rotate: 50,
                    stretch: 0,
                    depth: 100,
                    modifier: 1,
                    slideShadows: true,
                  }"
                  :pagination="true"
                  :modules="modules"
                  :navigation="true"
                >
                  <swiper-slide> <img src="../assets/img/gssd-project.png" /> </swiper-slide>
                  <swiper-slide> <img src="../assets/img/kalenapp.png"/> </swiper-slide>
                  <swiper-slide> <img src="../assets/img/maekornapp.png" /> </swiper-slide>
                  <swiper-slide> <img src="../assets/img/HealthEducation.png" /> </swiper-slide>
                  <swiper-slide> <img src="../assets/img/d2hdom.png" /> </swiper-slide>
                  <swiper-slide> <img src="../assets/img/seniorweb.png" /> </swiper-slide>
                </swiper>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper } from "../../node_modules/swiper/vue/swiper";
import { SwiperSlide } from "../../node_modules/swiper/vue/swiper-slide";
// Import Swiper styles
import "swiper/css/navigation";
import "../../node_modules/swiper/swiper.min.css";
import "../../node_modules/swiper/modules/effect-coverflow/effect-coverflow.min.css";
import "../../node_modules/swiper/modules/pagination/pagination.min.css";
import { Navigation } from "swiper";
import SwiperCore, { EffectCoverflow, Pagination, Autoplay } from "swiper";
SwiperCore.use([EffectCoverflow, Pagination, Autoplay]);
export default {
  name: "ProjectMe",
  components: {
    Swiper,
    SwiperSlide,
    
  },
  setup() {
    return {
      modules: [Navigation],
    };
  },
};
</script>

<style>

.content-project {
  z-index: 99 !important;
}

h2 > span {
  color: #0e82f3;
}

.swiper {
  width: 100%;
  padding-top: 50px;
  padding-bottom: 50px;
}
.swiper-slide {
  background-position: center;
  background-size: cover;
  width: 300px;
  height: 300px;
  font-size: 24px;
  font-weight: 700;
  display: flex;
  justify-content: center;
  align-items: center;
}

.swiper-slide img {
  display: block;
  width: 100%;
}
.swiper-slide:nth-child(1n) {
  background-color: palevioletred;
}
.swiper-slide:nth-child(2n) {
  background-color: skyblue;
}
.swiper-slide:nth-child(3n) {
  background-color: peru;
}
.swiper-slide:nth-child(4n) {
  background-color: cadetblue;
}
.swiper-slide:nth-child(5n) {
  background-color: plum;
}
.swiper-slide:nth-child(6n) {
  background-color: goldenrod;
}
.swiper-slide:nth-child(7n) {
  background-color: palegreen;
}

@media only screen and (max-width: 576px) {
  .swiper-button-next, .swiper-button-prev {
    display: none;
  }
}
</style>