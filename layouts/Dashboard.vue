<template lang="">
  <div class="main">
    <div class="d-flex">
      <transition name="slide">
        <aside v-if="togglesidebar">
          <!-- Sidebar content -->
          <SidebarContent @hidesidebar="hidesidebar" />
        </aside>
      </transition>

      <div class="container maincontent" style="width:flex-grow">
        <!-- Navbar -->
        <div>
          <NavBar @hidesidebar="hidesidebar" />
        </div>
        <!-- Main content -->
        <div>
          <Nuxt />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import NavBar from '~/components/Nav_Bar.vue'
import SidebarContent from '~/components/SidebarContent.vue'
export default {
  name: 'Dashboard',
  components:
  {
    NavBar,
    SidebarContent
  },
  data () {
    return {
      togglesidebar: 'true'
    }
  },
  methods:
  {
    hidesidebar (togglesidebar) {
      this.togglesidebar = togglesidebar
    },

    toggle () {
      this.togglesidebar = !this.togglesidebar
    }
  }
}
</script>
<style scoped>
.main
{
  background: #F5F5FB;
  height: 100vh;
  overflow: auto;
}
.slide-enter-active, .slide-leave-active {
  transition: transform 0.3s ease; /* Define the transition properties */
}

.slide-enter, .slide-leave-to {
  transform: translateX(-100%); /* Slide in or out the sidebar */
}
.maincontent
{
  overflow: auto;
  margin-left: 29%;
}
aside
{
  background: #FFFFFF;
  height: 100vh;
  width: 309px;
  font-family: 'Open Sans';
  position: fixed;
  top: 0;
      left: 0;
      bottom: 0;
      overflow-y: auto;
      box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.12);
}

aside::-webkit-scrollbar {
  width: 6px;
}

aside::-webkit-scrollbar-thumb {
  background-color: transparent;
}
@media screen and (max-width: 480px ){
  aside{
      width: 150px;
      z-index: 1000;
    }
    .maincontent
{
  margin-left: 0%;
}
}
</style>
