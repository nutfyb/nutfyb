<template>
  <section class="section-banner section-shaped my-0 bg-color-1 section-detailme">
    <div class="container d-flex">
      <div class="row justify-content-center">
        <div class="col-12 m-auto content-skill">
          <div class="content-skill-logo float-left text-white">
            <h2>My Skills and Expertise</h2>
            <h6>Programming Skills</h6>
          </div>
          <div class="skill">
            <div class="skill-logo">
              <img
                src="../assets/img/html-logo.png"
                alt="html-logo"
                width="60"
                class="logo-img"
              />
              <h6>HTML5</h6>
            </div>
            <div class="skill-logo">
              <img
                src="../assets/img/css-logo.png"
                alt="css-logo"
                width="60"
                class="logo-img"
              />
              <h6>CSS</h6>
            </div>
            <div class="skill-logo">
              <img
                src="../assets/img/js-logo.png"
                alt="js-logo"
                width="60"
                class="logo-img"
              />
              <h6>JavaScript</h6>
            </div>
            <div class="skill-logo">
              <img
                src="../assets/img/bootstrap-logo.png"
                alt="bootstrap-logo"
                width="60"
                class="logo-img"
              />
              <h6>Bootstrap</h6>
            </div>
            <div class="skill-logo">
              <img
                src="../assets/img/vue-logo.png"
                alt="vue-logo"
                width="60"
                class="logo-img"
              />
              <h6>Vue</h6>
            </div>
            <div class="skill-logo">
              <img
                src="../assets/img/php-logo.png"
                alt="php-logo"
                width="60"
                class="logo-img"
              />
              <h6>PHP</h6>
            </div>
            <div class="skill-logo">
              <img
                src="../assets/img/flutter-logo.png"
                alt="flutter-logo"
                width="60"
                class="logo-img"
              />
              <h6>Flutter</h6>
            </div>
            <div class="skill-logo">
              <img
                src="../assets/img/wordpress-logo.png"
                alt="wordpress-logo"
                width="60"
                class="logo-img"
              />
              <h6>WordPress</h6>
            </div>
            <div class="skill-logo">
              <img
                src="../assets/img/wix-logo.png"
                alt="wix-logo"
                width="60"
                class="logo-img"
              />
              <h6>Wix</h6>
            </div>
            <div class="skill-logo">
              <img
                src="../assets/img/python-logo.png"
                alt="python-logo"
                width="60"
                class="logo-img"
              />
              <h6>Python</h6>
            </div>
            <div class="skill-logo">
              <img
                src="../assets/img/gitlab-logo.png"
                alt="gitlab-logo"
                width="60"
                class="logo-img"
              />
              <h6>Gitlab</h6>
            </div>
            <div class="skill-logo">
              <img
                src="../assets/img/postman-logo.png"
                alt="postman-logo"
                width="60"
                class="logo-img"
              />
              <h6>Postman</h6>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "DetailMe",
};
</script>

<style>
.section-detailme {
  z-index: 999;
}
.bg-color-1 {
  background-color: #21272f;
}
.content-skill {
  margin-bottom: 2.5rem;
}
.content-skill-logo {
  margin-top: 2.5rem;
  margin-bottom: 2.5rem;
}
.skill {
  grid-template-columns: repeat(6, 1fr);
}
.skill-logo {
  width: 200px;
  text-align: center;
  display: block;
  background-color: transparent;
  border: 1px solid transparent;
  margin-right: 10px;
  margin-bottom: 2rem;
  float: left;
  color: #fff;
}
.logo-img {
  transition: 0.3s;
  transform: perspective(400px) scaleX(1);
}
.logo-img:hover {
  transform: perspective(400px) scaleX(-1);
}
.skill-logo > h6 {
  margin-top: 1rem;
}

@media only screen and (max-width: 768px) {
  .skill {
    margin: auto;
    width: 100%;
    padding: 10px;
  }
  .skill-logo {
    width: 45%;
    text-align: center;
    display: block;
    background-color: transparent;
    border: 1px solid transparent;
    margin-bottom: 2rem;
    float: left;
    color: #fff;
}
}

@media only screen and (max-width: 576px) {
  .skill {
    margin: auto;
    width: 50%;
    padding: 10px;
  }
  .skill-logo {
    width: 100%;
    text-align: center;
    display: block;
    background-color: transparent;
    border: 1px solid transparent;
    margin-right: 10px;
    margin-bottom: 2rem;
    color: #fff;
}
}

</style>