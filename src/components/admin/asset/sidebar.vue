<template>
  <div id="app" class="my-5">
       <nav class="sidebar sidebar-offcanvas" id="sidebar">
          <ul class="nav">
            <li class="nav-item nav-profile">
              <a href="#" class="nav-link">
                <div class="nav-profile-image">
                  <img src="@/assets/images/faces/face1.jpg" alt="profile">
                  <span class="login-status online"></span>
                  <!--change to offline or busy as needed-->
                </div>
                <div class="nav-profile-text d-flex flex-column">
                  <span class="font-weight-bold mb-2">Bokhtiar Toshar</span>
                  <span class="text-secondary text-small">Project Manager</span>
                </div>
                <i class="mdi mdi-bookmark-check text-success nav-profile-badge"></i>
              </a>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" :to="{path:'/dashboard' }">
                <span class="menu-title">Dashboard</span>
                <i class="mdi mdi-home menu-icon"></i>
              </router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link"  :to="{path: '/categories'}">
                <span class="menu-title">Categories</span>
                <i class="mdi mdi-certificate menu-icon"></i>
              </router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" :to="{path: '/brands'}">
                <span class="menu-title">Brands</span>
                <i class="mdi mdi-notification-clear-all menu-icon"></i>
              </router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" :to="{path: '/products'}">
                <span class="menu-title">Products</span>
                <i class="mdi mdi-desktop-mac menu-icon"></i>
              </router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" :to="{path: '/pos'}">
                <span class="menu-title">POS</span>
                <i class="mdi mdi-chart-bar menu-icon"></i>
              </router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link" :to="{path:'/customers'}">
                <span class="menu-title">Customers</span>
                <i class="mdi mdi-table-large menu-icon"></i>
              </router-link>
            </li>

            <li class="nav-item">
              <router-link class="nav-link" :to="{path:'/orders'}">
                <span class="menu-title">All Orders</span>
                <i class="mdi mdi-table-large menu-icon"></i>
              </router-link>
            </li>

            <li class="nav-item">
              <router-link class="nav-link" :to="{path:'/day/sell'}">
                <span class="menu-title">This Day Sell</span>
                <i class="mdi mdi-table-large menu-icon"></i>
              </router-link>
            </li>

            <li class="nav-item">
              <router-link class="nav-link" :to="{path:'/monthly/sell'}">
                <span class="menu-title">This Monthly Sell</span>
                <i class="mdi mdi-table-large menu-icon"></i>
              </router-link>
            </li>

            <li class="nav-item">
              <router-link class="nav-link" :to="{path:'/year/sell'}">
                <span class="menu-title">This Year Sell</span>
                <i class="mdi mdi-table-large menu-icon"></i>
              </router-link>
            </li>

            <li class="nav-item">
              <router-link class="nav-link" :to="{path:'/registration'}">
                <span class="menu-title">New Admin</span>
                <i class="mdi mdi-table-large menu-icon"></i>
              </router-link>
            </li>



          </ul>
        </nav>
  </div>
</template>

<script>
export default {

}
</script>

<style>

</style>
