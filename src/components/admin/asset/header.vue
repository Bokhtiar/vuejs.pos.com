<template>
  <div id="app">
    <nav
      class="
        navbar
        default-layout-navbar
        col-lg-12 col-12
        p-0
        fixed-top
        d-flex
        flex-row
      "
    >
      <div
        class="
          text-center
          navbar-brand-wrapper
          d-flex
          align-items-center
          justify-content-center
        "
      >
        <router-link class="navbar-brand brand-logo" :to="{path:'/'}"
          ><img src="@/assets/images/logo.svg" alt="logo"
        /></router-link>

      </div>
      <div class="navbar-menu-wrapper d-flex align-items-stretch">
        <button
          class="navbar-toggler navbar-toggler align-self-center"
          type="button"
          data-toggle="minimize"
        >
          <span class="mdi mdi-menu"></span>
        </button>

        <ul class="navbar-nav navbar-nav-right">
          <li class="nav-item nav-profile dropdown">
            <a
              class="nav-link dropdown-toggle"
              id="profileDropdown"
              href="#"
              data-toggle="dropdown"
              aria-expanded="false"
            >
              <div class="nav-profile-img">


              </div>
              <div class="nav-profile-text">
                <p class="mb-1 text-black">Bokhtiar Toshar</p><span class="availability-status online"></span>
              </div>
            </a>
            <div
              class="dropdown-menu navbar-dropdown"
              aria-labelledby="profileDropdown"
            >
              <a class="dropdown-item" href="#">
                <i class="mdi mdi-cached mr-2 text-success"></i> Activity Log
              </a>
              <div class="dropdown-divider"></div>
              <a class="dropdown-item" href="#">
                <i class="mdi mdi-logout mr-2 text-primary"></i> Signout
              </a>
            </div>
          </li>
          <li class="nav-item d-none d-lg-block full-screen-link">
            <a class="nav-link">
              <i class="mdi mdi-fullscreen" id="fullscreen-button"></i>
            </a>
          </li>

          <li class="nav-item nav-logout d-none d-lg-block">
            <router-link class="nav-link" :to="{path: '/logout'}">
              <i class="mdi mdi-power"></i>
            </router-link>
          </li>
        </ul>
        <button
          class="
            navbar-toggler navbar-toggler-right
            d-lg-none
            align-self-center
          "
          type="button"
          data-toggle="offcanvas"
        >
          <span class="mdi mdi-menu"></span>
        </button>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  data(){
    return{
      keyword: '',
    }
  },
  methods:{
    search(){
      this.$emit('search', this.keyword)
    }
  },

   mounted(){
    token = localStorage.getItem('AToken')
  }
};
</script>

<style>
</style>
