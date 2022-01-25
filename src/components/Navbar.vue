<template>
  <nav
    class="navbar navbar-expand-lg navbar-dark fixed-top"
    :class="{
      'navbar-shrink': navbarShrink,
    }"
    id="mainNav"
  >
    <div class="container">
      <a class="navbar-brand" href="#page-top"
        ><img :src="require('@/assets/img/logo-transparent-2.png')" alt="..."
      /></a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarResponsive"
        aria-controls="navbarResponsive"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        Menu
        <i class="fas fa-bars ms-1"></i>
      </button>
      <div class="collapse navbar-collapse" id="navbarResponsive">
        <ul class="navbar-nav text-uppercase ms-auto py-4 py-lg-0">
          <li class="nav-item">
            <a class="nav-link" href="#services">最新消息</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#registration">報名表</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#video">影片</a>
          </li>
          <li class="nav-item"><a class="nav-link" href="#team">成員</a></li>
          <!-- <li class="nav-item">
            <a class="nav-link" href="#contact">Contact</a>
          </li> -->
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data: () => ({
    navbarShrink: true,
  }),
  mounted() {
    window.addEventListener("scroll", this.onScroll);
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.onScroll);
  },
  methods: {
    onScroll(e) {
      const window = e.currentTarget;
      this.navbarShrink = window.scrollY === 0;
    },
  },
};
</script>

<style scoped>
.nav-link {
  font-family: "Architects Daughter", cursive !important;
  color: #000 !important;
  font-size: 1.3rem !important;
}
.nav-link:hover {
  font-family: "Architects Daughter", cursive !important;
  color: #fff !important;
}
</style>
