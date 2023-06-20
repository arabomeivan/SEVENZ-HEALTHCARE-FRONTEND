<template lang="">
  <div class="main">
    <div class="d-flex">
      <aside>
        <!-- Sidebar content -->
        <h3>Sidebar</h3>
        <ul>
          <li>Menu Item 1</li>
          <li>Menu Item 2</li>
          <li>Menu Item 3</li>
        </ul>
      </aside>

      <div class="container maincontent" style="width:flex-grow">
        <!-- Navbar -->
        <div>
          <NavBar />
        </div>
        <!-- Main content -->
        <Nuxt />
      </div>
    </div>
  </div>
</template>
<script>
import NavBar from '~/components/Nav_Bar.vue'
export default {
  name: 'Dashboard',
  components:
  {
    NavBar
  }
}
</script>
<style scoped>
.main
{
  background: #F5F5FB;
  height: 100vh;
}
.maincontent
{
  overflow: auto;
  margin-left: 25%;
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
}

@media screen and (max-width: 480px ){
  aside{
      width: 150px;
      z-index: 1000;
    }
    .maincontent
{
  overflow: auto;
  margin-left: 37%;
}
}
</style>
