<template>
  <div>
    <NavigationMobile />
    <!-- <PageLoader /> -->
    <div class="content" :class="{ open: showNav }">
      <div class="top-bar">
        <nav
          class="
            navbar navbar-dark
            justify-content-between
            flex-nowrap flex-row
          "
        >
          <div class="container res-mobile">
            <a class="navbar-brand float-left"><b>Anuthep</b></a>
            <ul class="nav navbar-nav flex-row float-right">
              <li class="nav-item">
                <div
                  id="navigation-icon"
                  v-if="mobileView"
                  @click="opensidebar"
                >
                  <i class="fas fa-bars"></i>
                </div>
              </li>
            </ul>
          </div>
        </nav>
        <NavigationBar v-if="!mobileView" />
      </div>
      <transition name="fade">
        <div id="pagetop" class="fixed" v-show="scY > 300" @click="toTop">
          <div class="icontooltip">
            <span class="tooltip">Up to page.</span>
            <span><font-awesome-icon icon="fa-solid fa-circle-up" /></span>
          </div>
        </div>
      </transition>
    </div>
  </div>
  <TopBanner />
  <DetailMe />
  <HistoryExperience />
  <ProjectMe />
  <SecFooter />
</template>
<script>
import TopBanner from "./components/TopBanner.vue";
import DetailMe from "./components/DetailMe.vue";
import HistoryExperience from "./components/HistoryExperience.vue";
import ProjectMe from "./components/ProjectMe.vue";
import SecFooter from "./components/SecFooter.vue";
// import PageLoader from "./components/PageLoader.vue";
import NavigationBar from "./components/NavigationBar.vue";
import NavigationMobile from "./components/NavigationMobile.vue";
export default {
  data: () => {
    return {
      mobileView: true,
      showNav: false,
      scTimer: 0,
      scY: 0,
      variant: "dark",
      variants: [
        "transparent",
        "white",
        "light",
        "dark",
        "primary",
        "secondary",
        "success",
        "danger",
        "warning",
        "info",
      ],
    };
  },
  components: {
    TopBanner,
    DetailMe,
    HistoryExperience,
    ProjectMe,
    SecFooter,
    // PageLoader,
    NavigationBar,
    NavigationMobile,
  },
  methods: {
    handleView() {
      this.mobileView = window.innerWidth <= 990;
    },
    opensidebar() {
      document.getElementById("mySidenav").style.width = "250px";
    },
    handleScroll: function () {
      if (this.scTimer) return;
      this.scTimer = setTimeout(() => {
        this.scY = window.scrollY;
        clearTimeout(this.scTimer);
        this.scTimer = 0;
      }, 100);
    },
    toTop: function () {
      window.scrollTo({
        top: 0,
        behavior: "smooth",
      });
    },
  },
  created() {
    this.handleView();
    window.addEventListener("resize", this.handleView);
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
};
</script>
<style lang="scss">
@import url("https://use.fontawesome.com/releases/v5.9.0/css/all.css");

html {
  scroll-behavior: smooth;
}

#pagetop {
  display: block;
  position: fixed;
  right: -75px;
  bottom: 10px;
  font-size: 40px;
  width: 10%;
  color: var(--white);
  z-index: 9999;
}

#pagetop:hover .tooltip {
  top: 80px;
  opacity: 1;
  visibility: visible;
  pointer-events: auto;
}

.icontooltip .tooltip::before {
  position: absolute;
  content: "";
  height: 8px;
  width: 8px;
  background: var(--blue);
  bottom: -3px;
  left: 50%;
  transform: translate(-50%) rotate(45deg);
  transition: all 0.3s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

#pagetop .icontooltip:hover .tooltip {
  top: -45px;
  opacity: 1;
  visibility: visible;
  pointer-events: auto;
  background: var(--blue);
  color: #ffffff;
}
.icontooltip svg {
  margin-left: 23px;
}

.icontooltip svg:hover {
  color: var(--blue);
}

.tooltip {
  position: absolute;
  top: 0;
  font-size: 14px;
  background: #ffffff;
  color: #ffffff;
  padding: 5px 8px;
  border-radius: 5px;
  box-shadow: 0 10px 10px rgb(0 0 0 / 10%);
  opacity: 0;
  pointer-events: none;
  transition: all 0.3s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

.top-bar {
  display: flex;
  width: 100%;
}

.open {
  transform: translateX(300px);
}

.fa-bars {
  color: var(--white);
}

@media only screen and (max-width: 1600px) {
  #pagetop {
    right: -15px;
  }
}

@media only screen and (max-width: 576px) {
  #pagetop {
    right: 35px;
  }
  #pagetop:hover .tooltip {
    display: none;
  }
  div.container.res-mobile {
    margin-right: 20px;
  }
}


:root {
  --white: #ffffff;
  --black: #000000;
  --black01: #21272f;
  --blue: #0d6efd;
}
</style>