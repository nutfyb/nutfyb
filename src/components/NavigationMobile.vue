<template>
  <div id="mySidenav" class="sidenav">
    <a class="closebtn" @click="closesidebar"
      ><font-awesome-icon icon="fa-solid fa-xmark"
    /></a>
    <a href="#home"
      ><font-awesome-icon icon="fa-solid fa-house" /><span>Home</span></a
    >
    <a href="#experience"
      ><font-awesome-icon icon="fa-solid fa-bars-progress" /><span
        >Experience</span
      ></a
    >
    <a href="#project"
      ><font-awesome-icon icon="fa-solid fa-diagram-project" /><span
        >Project</span
      ></a
    >
    <div class="container contact-info">
      <h4>Contact Info</h4>
      <ul class="contact-ul">
        <li class="contact-address">
          38 White Box Apartment Ramkhamhaeng 18 Bangkapi District, Bangkok,
          10240
        </li>
        <li><a href="tel:0652377015" class="contact-a"><font-awesome-icon icon="fa-solid fa-phone" />065-2377015</a></li>
        <li>
          <a href="mailto:anuthep.tayngam@gmail.com" class="contact-b"><font-awesome-icon icon="fa-solid fa-envelope" />anuthep.tayngam@gmail.com</a>
        </li>
      </ul>
    </div>
  </div>
</template>
  
  <script>
export default {
  name: "NavigationMobile",
  methods: {
    closesidebar() {
      document.getElementById("mySidenav").style.width = "0%";
    },
  },
};
</script>
  
  <style lang="scss" scoped>
  li.contact-address {
    font-size: 12px !important;
    padding-bottom: 15px;
  }
.sidenav a span {
  padding-left: 5px;
}
.contact-info {
  position: relative;
  padding: 120px 30px 20px 30px;
  color: var(--white);
}
.contact-ul {
  padding: 0;
}
.contact-a {
  padding: 0 !important;
  font-size: 10px;
  text-decoration: none;
  border-top: 0px !important;
}
.contact-a:hover {
  background-color: var(--black) !important;
  color: var(--white) !important;
}
.contact-a svg {
    padding-right: 5px;
}
.contact-b {
  padding: 0 !important;
  font-size: 10px;
  text-decoration: none;
  border-top: 0px !important;
}
.contact-b:hover {
  background-color: var(--black) !important;
  color: var(--white) !important;
}
.contact-b svg {
    padding-right: 5px;
}
.contact-info ul li {
  position: relative;
  display: block;
  font-size: 15px;
  color: rgba(255, 255, 255, 0.8);
  margin-bottom: 3px;
}
.fa-xmark:hover {
  transform: rotate(360deg);
  transition: transform 0.7s ease-in-out;
}
.sidenav {
  height: 100%;
  width: 0;
  position: fixed;
  z-index: 9999;
  top: 0;
  right: 0;
  background-color: var(--black);
  overflow-x: hidden;
  transition: 0.5s;
  padding-top: 60px;
}

.sidenav a {
  position: relative;
  display: block;
  line-height: 24px;
  padding: 18px 25px;
  font-weight: 500;
  color: #ffffff;
  text-transform: uppercase;
  transition: all 500ms ease;
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  text-decoration: none;
}
.sidenav a:hover {
  background-color: var(--white);
  color: var(--black);
}

.sidenav .closebtn {
  position: absolute;
  top: 0;
  right: 25px;
  font-size: 36px;
  margin-left: 50px;
}

@media screen and (max-height: 450px) {
  .sidenav {
    padding-top: 15px;
  }
  .sidenav a {
    font-size: 18px;
  }
}
</style>