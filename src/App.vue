<template>
  <div id="app">
    <b-navbar toggleable="lg" type="light" variant="faded" class="navbar-white" fixed="top">
      <b-container>
        <b-navbar-brand to="/" style="navbar-brand">
          <img
            src="./assets/virus.png"
            class="d-inline-block align-top mr-1"
            alt="Covid"
            height="30"
            width="30"
          />COVID-19
        </b-navbar-brand>
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav class="ml-auto">
            <b-navbar-nav>
              <b-nav-item class="mr-4" to="/" exact>Beranda</b-nav-item>
              <b-nav-item class="mr-4" to="/news" exact>Berita</b-nav-item>
              <b-nav-item class="mr-1" v-b-modal.modalku>Tentang</b-nav-item>
            </b-navbar-nav>
          </b-navbar-nav>
        </b-collapse>
      </b-container>
    </b-navbar>
    <router-view />
    <footer class="mt-5 footer">
      <h6 class="text-center footer-text">
        Copyright 2020
        <a href="https://github.com/ihsaninh" class="text-link">Ihsan Nurul Habib</a> | Sumber
        data berasal dari API
        <a
          href="https://github.com/mathdroid/covid-19-api"
          class="text-link"
        >Mathdroid</a>
      </h6>
    </footer>
    <vm-back-top timing="ease">
      <button class="btn-to-top">
        <svg
          aria-hidden="true"
          focusable="false"
          data-prefix="fas"
          data-icon="arrow-up"
          role="img"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 448 512"
          class="icon-to-top"
        >
          <path
            fill="currentColor"
            d="M34.9 289.5l-22.2-22.2c-9.4-9.4-9.4-24.6 0-33.9L207 39c9.4-9.4 24.6-9.4 33.9 0l194.3 194.3c9.4 9.4 9.4 24.6 0 33.9L413 289.4c-9.5 9.5-25 9.3-34.3-.4L264 168.6V456c0 13.3-10.7 24-24 24h-32c-13.3 0-24-10.7-24-24V168.6L69.2 289.1c-9.3 9.8-24.8 10-34.3.4z"
          />
        </svg>
      </button>
    </vm-back-top>
    <b-modal id="modalku" title="Tentang Web COVID-19" hide-footer>
      <p>
        Aplikasi ini ditujukan hanya untuk keperluan informasi belaka dan tidak
        untuk komersial. Semua data yang ditampilkan merupakan hasil dari data
        John Hopkins University CSSE.
      </p>
    </b-modal>
  </div>
</template>

<script>
import VmBackTop from "vue-multiple-back-top";

export default {
  name: "App",
  components: {
    VmBackTop
  }
};
</script>
<style>
#app {
  font-family: "Roboto";
}
th {
  font-weight: 500;
  font-size: 15px;
}
td {
  font-size: 14px !important;
}
body {
  background-color: #fefefe !important;
  color: #485460;
}
.navbar-white {
  background-color: rgba(255, 255, 255, 0.7) !important;
  box-shadow: 0 0 32px -4px rgba(0, 0, 0, 0.08);
  backdrop-filter: saturate(180%) blur(20px);
}
.navbar-light .navbar-brand {
  color: inherit;
  background: linear-gradient(to right, #30cfd0 0%, #218c74 100%);
  background-clip: text;
  -webkit-text-fill-color: transparent;
}
.navbar-light .navbar-nav .nav-link.active {
  color: inherit;
}
.navbar-brand {
  font-weight: 500 !important;
  font-size: 22px !important;
}
.footer {
  padding-top: 35px;
  padding-bottom: 30px;
  background-color: #fff;
  border-top: 1px solid #f1f1f1;
}
.footer h6 {
  font-weight: 400;
  font-size: 15px;
}
.btn-to-top {
  width: 60px;
  height: 60px;
  padding: 10px 16px;
  border-radius: 50%;
  font-size: 22px;
  line-height: 22px;
  background-color: #5aaa4e;
  color: white;
  outline: none !important;
  border: none;
}
.icon-to-top {
  width: 20px;
}
.modal-content {
  border: none !important;
  font-family: Roboto;
  border-radius: 5px !important;
  box-shadow: 0 0 4px 0 rgba(0, 0, 0, 0.01), 0 4px 24px 0 rgba(0, 0, 0, 0.05);
}
.modal-header {
  border-bottom: 1px solid #f1f1f1 !important;
}
.modal-body p {
  font-size: 15px;
  line-height: 26px;
}
.modal-title {
  font-size: 18px;
}
.modal-header .close {
  display: none;
}
.footer-text {
  font-weight: 300 !important;
}
.text-link {
  color: #5aaa4e;
}
.text-link:hover {
  color: #4d9143;
}
.table {
  color: inherit !important;
}
@media only screen and (min-width: 768px) {
  .navbar {
    height: 70px;
  }
}
@media only screen and (max-width: 768px) {
  h6 {
    font-size: 15px !important;
  }
  th {
    font-weight: 500;
    font-size: 13px;
  }
  td {
    font-size: 13px !important;
  }
}
</style>
