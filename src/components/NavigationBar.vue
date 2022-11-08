<template>
    <div id="navigationbar">
        <nav
      class="navbar navbar-dark justify-content-between flex-nowrap flex-row"
    >
      <div class="container">
        <a class="navbar-brand float-left"><b>Anuthep</b></a>
        <ul class="nav navbar-nav flex-row float-right">
          <li class="nav-item">
            <a class="nav-link" href="#home">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#experience">Experience</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#project">Project</a>
          </li>
          <li class="nav-item">
          </li>
        </ul>
      </div>
    </nav>
    </div>
</template>

<script>
export default {
    name: "NavigationBar",
}
</script>

<style>

nav {
  position: fixed !important;
  width: 100vw;
  top: 0;
  left: 0;
  z-index: 998;
  background-color: transparent;
}
.nav-item {
  margin-left: 15px;
}
</style>