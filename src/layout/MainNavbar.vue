<template>
    <navbar position="fixed"
            type="info"
            :transparent="false"
            :color-on-scroll="colorOnScroll"
            menu-classes="ml-auto"
           >
        <template>
            <router-link v-popover:popover1 class="navbar-brand" to="/">
               WEB PERSONAL
            </router-link>
            <el-popover ref="popover1"
                        popper-class="popover"
                        placement="bottom"
                        width="200"
                        trigger="hover">
                <div class="popover-body">
                    Designed by Invision. Coded by Javier Velazquez
                </div>
            </el-popover>
        </template>
        <template slot="navbar-menu">
            <li class="nav-item">
                <a class="nav-link"
                   href="https://www.creative-tim.com/product/vue-now-ui-kit"
                   target="_blank">
                    <i class="now-ui-icons arrows-1_cloud-download-93"></i>
                    <p>Download</p>
                </a>
            </li>
            <drop-down tag="li"
                       title="Components"
                       icon="now-ui-icons design_app"
                       class="nav-item">
                <nav-link to="/">
                    <i class="now-ui-icons business_chart-pie-36"></i> All components
                </nav-link>
                <a href="https://demos.creative-tim.com/vue-now-ui-kit/documentation"
                   target="_blank"
                   class="dropdown-item">
                    <i class="now-ui-icons design_bullet-list-67"></i> Documentation
                </a>
            </drop-down>
            <drop-down tag="li"
                       title="Examples"
                       icon="now-ui-icons design_image"
                       class="nav-item">
                <nav-link to="/landing">
                    <i class="now-ui-icons education_paper"></i> Landing
                </nav-link>
                <nav-link to="/login">
                    <i class="now-ui-icons users_circle-08"></i> Login
                </nav-link>
                <nav-link to="/profile">
                    <i class="now-ui-icons users_single-02"></i> Profile
                </nav-link>
            </drop-down>
            

            <li class="nav-item">
                <a class="nav-link"
                   rel="tooltip"
                   title="Follow us on Twitter"
                   data-placement="bottom"
                    href="https://www.linkedin.com/in/javier-vel%C3%A1zquez-45747015/"
                   target="_blank">
                    <i class="fab fa-linkedin"></i>
                    <p class="d-lg-none d-xl-none">Linkedin</p>
                </a>
            </li>
            <li class="nav-item">
                <a class="nav-link"
                   rel="tooltip"
                   title="Like us on Facebook"
                   data-placement="bottom"
                    href="https://github.com/javiervelaz"
                   target="_blank">
                    <i class="fab fa-github"></i>
                    <p class="d-lg-none d-xl-none">Github</p>
                </a>
            </li>
            
        </template>
    </navbar>
</template>


<script>
import { DropDown, Navbar, NavLink } from '@/components';
import { Popover } from 'element-ui';
export default {
  name: 'main-navbar',
  props: {
    transparent: Boolean,
    colorOnScroll: Number
  },
  components: {
    DropDown,
    Navbar,
      NavLink,
    [Popover.name]: Popover
  }
};
</script>

<style scoped></style>
