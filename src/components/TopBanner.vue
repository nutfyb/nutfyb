<template>
  <section class="section-banner section-shaped my-0 bg-color-3" id="home">
    <div class="container d-flex">
      <div class="row justify-content-center">
        <div class="col-12 col-sm-6 m-auto content-bio">
          <div class="float-left text-white">
            <h6>Hello, I'm</h6>
            <h2>Anuthep Tayngam</h2>
            <div class="box-text">
              <h4 class="word1">Front-End Developer</h4>
            </div>
            <p>
              I love to learn about new technologies.I am looking for a
              full-time of junior front-end position. I am able to work under
              pressure and cope well in various working environments. I always
              enjoy learning and improving myself so that I can grow with the
              organization together.
            </p>
            <a href="#Contact-me">
              <button type="button" class="btn btn-outline-light">
                Contact me
              </button></a
            >
            <a href="https://drive.google.com/file/d/1ZhhGU99-JLarcE4I7vZt3EnVEejXDSx1/view?usp=sharing" target="_blank">
            <button type="button" class="btn btn-outline-light">
              Get Resume
            </button>
          </a>
          </div>
        </div>
        <div class="col-12 col-sm-6 img-frame">
          <img src="../assets/img/nut.png" alt="me" class="img-center" />
            <ul class="particle">
              <li></li>
              <li></li>
              <li></li>
              <li></li>
              <li></li>
              <li></li>
              <li></li>
              <li></li>
              <li></li>
              <li></li>
            </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "TopBanner",
};
</script>

<style>

/* .particle-container{ 
    width: 100%;
} */
#home {
  height: 50%;
}
.particle{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 475px;
    overflow: hidden;
    z-index: 1;
}

.particle li{
    position: absolute;
    display: block;
    list-style: none;
    width: 20px;
    height: 20px;
    background: rgba(255, 255, 255, 0.2);
    animation: animate 25s linear infinite;
    bottom: -150px;
    
}

.particle li:nth-child(1){
    left: 25%;
    width: 80px;
    height: 80px;
    animation-delay: 0s;
}

.particle li:nth-child(2){
    left: 10%;
    width: 20px;
    height: 20px;
    animation-delay: 2s;
    animation-duration: 12s;
}

.particle li:nth-child(3){
    left: 70%;
    width: 20px;
    height: 20px;
    animation-delay: 4s;
}

.particle li:nth-child(4){
    left: 40%;
    width: 60px;
    height: 60px;
    animation-delay: 0s;
    animation-duration: 18s;
}

.particle li:nth-child(5){
    left: 65%;
    width: 20px;
    height: 20px;
    animation-delay: 0s;
}

.particle li:nth-child(6){
    left: 75%;
    width: 110px;
    height: 110px;
    animation-delay: 3s;
}

.particle li:nth-child(7){
    left: 35%;
    width: 150px;
    height: 150px;
    animation-delay: 7s;
}

.particle li:nth-child(8){
    left: 50%;
    width: 25px;
    height: 25px;
    animation-delay: 15s;
    animation-duration: 45s;
}

.particle li:nth-child(9){
    left: 20%;
    width: 15px;
    height: 15px;
    animation-delay: 2s;
    animation-duration: 35s;
}

.particle li:nth-child(10){
    left: 85%;
    width: 150px;
    height: 150px;
    animation-delay: 0s;
    animation-duration: 11s;
}



@keyframes animate {

    0%{
        transform: translateY(0) rotate(0deg);
        opacity: 1;
        border-radius: 0;
    }

    100%{
        transform: translateY(-1000px) rotate(720deg);
        opacity: 0;
        border-radius: 50%;
    }

}

/* ------------------------------------------------ */

.content-bio {
  z-index: 999;
}

.btn {
  margin-right: 15px;
}
.img-center {
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 50%;
  z-index: 999;
}
.img-frame {
  height: 100%;
}
.box-text {
  background-color: white;
  color: #333;
  display: block;
  font-weight: 900;
  overflow: hidden;
  padding-left: 0.5rem;
  position: relative;
  margin-bottom: 10px;
  animation: openclose 15s ease-in-out infinite;
  white-space: nowrap;
}

@keyframes openclose {
  0% {
    width: 0;
  }
  5% {
    width: 0;
  }
  15% {
    width: 245px;
  }
  30% {
    width: 245px;
  }
  33% {
    width: 0;
  }
  35% {
    width: 0;
  }
  38% {
  }
  48% {
    width: 245px;
  }
  62% {
    width: 245px;
  }
  66% {
    width: 0;
    text-indent: 0;
  }
  71% {
    width: 0;
    text-indent: 5px;
  }
  86% {
    width: 245px;
  }
  95% {
    width: 245px;
  }
  98% {
    width: 0;
    text-indent: 5px;
  }
  100% {
    width: 0;
    text-indent: 0;
  }
}



@media only screen and (max-width: 1399px) {
  .particle {
    top: -65px;
  }
}

@media only screen and (max-width: 1199px) {
  .particle {
    top: -55px;
  }
  #home {
    height: 45vh;
  }
}

@media only screen and (max-width: 991px) {
  #home {
    height: 55vh;
}
  .particle {
    top: 35px;
  }
}


@media only screen and (max-width: 575px) {
  #home {
    height: 90vh;
}
  .particle {
    top: 360px;
  }
}
</style>