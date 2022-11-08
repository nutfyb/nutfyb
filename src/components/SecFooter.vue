<template>
  <section
    class="section-banner section-shaped my-0 bg-color-3"
    id="Contact-me"
  >
    <div class="container d-flex section-footer">
      <ul class="box-animation">
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
      </ul>
      <ul class="box-animation-y">
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
      </ul>
      <div class="row m-auto justify-content-center w-100 h-40">
        <div class="col-12 m-auto content-skill">
          <div class="content-skill-logo text-white text-center">
            <h2>Contact me</h2>
            <h6>
              <span
                ><a
                  href="mailto:anuthep.tayngam@gmail.com"
                  id="style-2"
                  class="mailme"
                  data-replace="anuthep.tayngam@gmail.com"
                  ><span>anuthep.tayngam@gmail.com</span></a
                ></span
              >
              <span class="space">|</span>
              <span
                ><a
                  href="tel:065-2377015"
                  id="style-2"
                  class="mailme"
                  data-replace="065-2377015"
                  ><span>065-2377015</span></a
                ></span
              >
            </h6>
            <ul class="social-icons">
              <li>
                <a href="https://www.facebook.com/nut.chur/" target="_blank"
                  ><font-awesome-icon icon="fa-brands fa-facebook-f"
                /></a>
              </li>
              <li>
                <a href="https://www.instagram.com/nut_phur/" target="_blank"
                  ><font-awesome-icon icon="fa-brands fa-instagram"
                /></a>
              </li>
              <li>
                <a
                  href="https://www.linkedin.com/in/anuthap-tayngam-10a547219"
                  target="_blank"
                  ><font-awesome-icon icon="fa-brands fa-linkedin-in"
                /></a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section
    class="
      section-banner section-shaped
      my-0
      bg-color-3
      d-flex
      justify-content-center
      text-white
      footer-copyright
    "
  >
    <p>© 2022 Copyright</p>
  </section>
</template>

<script>
export default {
  name: "SecFooter",
};
</script>


<style lang="scss">
.content-skill {
  z-index: 9999;
}

.bg-color-3 {
  display: flex;
  align-items: center;
  justify-content: center;
  background-size: 300% 300%;
  background-image: linear-gradient(
    -45deg,
    rgba(59, 173, 227, 1) 0%,
    rgba(87, 111, 230, 1) 25%,
    rgba(152, 68, 183, 1) 51%,
    rgba(255, 53, 127, 1) 100%
  );
  animation: AnimateBG 20s ease infinite;
}

@keyframes AnimateBG {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}

.footer-copyright {
  border-top: 1px solid #eaeaea;
}
.footer-copyright > p {
  padding-top: 0.5rem;
}
.space {
  overflow: hidden;
  position: relative;
  display: inline-block;
}
.mailme {
  overflow: hidden;
  position: relative;
  display: inline-block;
  margin-left: 0.5rem;
  margin-right: 0.5rem;
}

.mailme::before,
.mailme::after {
  content: "";
  position: absolute;
  width: 100%;
  left: 0;
}
.mailme::before {
  background-color: #fff;
  height: 2px;
  bottom: 0;
  transform-origin: 100% 50%;
  transform: scaleX(0);
  transition: transform 0.3s cubic-bezier(0.76, 0, 0.24, 1);
}
.mailme::after {
  content: attr(data-replace);
  height: 100%;
  top: 0;
  transform-origin: 100% 50%;
  transform: translate3d(200%, 0, 0);
  transition: transform 0.3s cubic-bezier(0.76, 0, 0.24, 1);
  color: #fff;
}
.mailme:hover::before {
  transform-origin: 0% 50%;
  transform: scaleX(1);
}
.mailme:hover::after {
  transform: translate3d(0, 0, 0);
}
.mailme span {
  display: inline-block;
  transition: transform 0.3s cubic-bezier(0.76, 0, 0.24, 1);
}

.mailme:hover span {
  transform: translate3d(-200%, 0, 0);
}

.bg-color-2 {
  background-color: #0e82f3;
}
.h-40 {
  height: 50vh;
}
.mailme {
  color: #fff;
  text-decoration: none;
}
.social-icons {
  padding: 0;
  list-style: none;
  margin: 1em;
}

.social-icons li {
  display: inline-block;
  margin: 0.15em;
  position: relative;
  font-size: 1em;
}

.social-icons svg {
  color: #0e82f3;
  position: absolute;
  top: 0.95em;
  left: 0.96em;
  transition: all 265ms ease-out;
}

.social-icons a {
  display: inline-block;
}

.social-icons a:before {
  transform: scale(1);
  -ms-transform: scale(1);
  -webkit-transform: scale(1);
  content: " ";
  width: 45px;
  height: 45px;
  border-radius: 25%;
  display: block;
  background: linear-gradient(45deg, #fff, #fff);
  transition: all 265ms ease-out;
}

.social-icons a:hover:before {
  transform: scale(0);
  transition: all 265ms ease-in;
}

.social-icons a:hover svg {
  transform: scale(2.2);
  -ms-transform: scale(2.2);
  -webkit-transform: scale(2.2);
  color: #fff;
  background: -webkit-linear-gradient(45deg, #ff003c, #c648c8);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  transition: all 265ms ease-in;
}
.section-footer {
  position: relative;
}
.box-animation {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  z-index: 1;
}
.box-animation li {
  position: absolute;
  display: block;
  list-style: none;
  width: 200px;
  height: 200px;
  border: 3px solid rgba(255, 255, 255, 0.2);
  animation: animatebox 25s linear infinite;
  bottom: -150px;
}
.box-animation li:nth-child(1) {
  width: 300px;
  height: 300px;
  left: 27vw;
  top: 42vh;
  animation-delay: 0s;
}

.box-animation li:nth-child(2) {
  left: 10%;
  width: 150px;
  height: 150px;
  border: 3px dotted rgba(255, 255, 255, 0.2);
  border-radius: 50%;
  animation-delay: 0s;
  animation-duration: 12s;
}

.box-animation li:nth-child(3) {
  left: 70%;
  width: 20px;
  height: 20px;
  border: 3px dotted rgba(255, 255, 255, 0.2);
  border-radius: 50%;
  animation-delay: 0s;
  animation-duration: 12s;
}

.box-animation li:nth-child(4) {
  left: 0;
  width: 20px;
  height: 20px;
  background: rgba(255, 255, 255, 0.2);
  border-radius: 50%;
  animation-delay: 0s;
  animation-duration: 12s;
}

.box-animation li:nth-child(5) {
  bottom: -50%;
  left: 75%;
  width: 60px;
  height: 60px;
  border: 3px dotted rgba(255, 255, 255, 0.2);
}

.box-animation li:nth-child(6) {
  top: 90%;
  left: 85%;
  width: 20px;
  height: 20px;
  background: rgba(255, 255, 255, 0.2);
}

@keyframes animatebox {
  0% {
    transform: translateY(-310px) rotate(0deg);
    opacity: 1;
  }

  100% {
    transform: translateY(-310px) rotate(720deg);
    opacity: 1;
  }
}

@media only screen and (max-width: 1669px) {
.box-animation li:nth-child(1) {
  left: 510px;
}
}
@media only screen and (max-width: 1399px) {
.box-animation li:nth-child(1) {
  left: 420px;
}
}

@media only screen and (max-width: 1199px) {
.box-animation li:nth-child(1) {
  left: 330px;
}
}

@media only screen and (max-width: 991px) {
.box-animation li:nth-child(1) {
  left: 210px;
}
}

@media only screen and (max-width: 767px) {
.box-animation li:nth-child(1) {
  left: 120px;
}
}

@media only screen and (max-width: 575px) {
  .box-animation li:nth-child(1) {
  left: 120px;
}
}

// box-animation-y

.box-animation-y {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  z-index: 1;
}
.box-animation-y li {
  position: absolute;
  display: block;
  list-style: none;
  width: 200px;
  height: 200px;
  border: 3px solid rgba(255, 255, 255, 0.2);
  animation: animatebox-y 25s linear infinite;
  animation-direction: alternate;
  bottom: -150px;
}
.box-animation-y li:nth-child(1) {
  top: 40%;
  left: 85%;
  width: 50px;
  height: 50px;
  background-color: rgba(255, 255, 255, 0.2);
  border: 3px dotted rgba(255, 255, 255, 0.2);
  animation-delay: 0s;
}

.box-animation-y li:nth-child(2) {
  top: 90%;
  left: 85%;
  width: 150px;
  height: 150px;
  border: 3px dotted rgba(255, 255, 255, 0.2);
  border-radius: 50%;
  animation-delay: 0s;
  animation-duration: 12s;
}

.box-animation-y li:nth-child(3) {
  top: 0;
  left: 70%;
  width: 20px;
  height: 20px;
  border: 3px dotted rgba(255, 255, 255, 0.2);
  border-radius: 50%;
  animation-delay: 0s;
  animation-duration: 12s;
}

.box-animation-y li:nth-child(4) {
  top: 25%;
  left: 20%;
  width: 20px;
  height: 20px;
  background: rgba(255, 255, 255, 0.2);
  border-radius: 50%;
  animation-delay: 0s;
  animation-duration: 12s;
}

.box-animation-y li:nth-child(5) {
  top: 10%;
  left: 30%;
  width: 60px;
  height: 60px;
  border: 3px dotted rgba(255, 255, 255, 0.2);
}

.box-animation-y li:nth-child(6) {
  top: 75%;
  left: 30%;
  width: 20px;
  height: 20px;
  background: rgba(255, 255, 255, 0.2);
  animation-duration: 8s;
}

@keyframes animatebox-y {
  0% {
    transform: translateX(0px) rotate(0deg);
    opacity: 1;
  }

  100% {
    transform: translateX(-310px) rotate(720deg);
    opacity: 1;
  }
}
</style>