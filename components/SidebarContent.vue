<template lang="">
  <div>
    <div class="toggler">
      <button
        class="navbar-toggler"
        type="button"
        style="margin-top: 5%;
    margin-left: 60%;"
        @click="hidesidebar"
      >
        <i class="fa-sharp fa-solid fa-grip" />
      </button>
    </div>
    <ul class="nav flex-column gap-4" style="margin-top:150px;">
      <li class="nav-item ">
        <a class="nav-link active" aria-current="page" href="#"> <span class="d-flex icons" style="margin-left:29px; margin-right:24px;"><img src="../static/dashboard.png" class="img-fluid align-self-center" alt=""></img></span><span class="align-self-center"> Dashboard</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#"><span class="d-flex icons" style="margin-left:29px; margin-right:24px;"><img src="../static/profile.png" class="img-fluid align-self-center" alt=""></img></span><span class="align-self-center">Profile</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#"><span class="d-flex icons" style="margin-left:29px; margin-right:24px;"><img src="../static/services.png" class="img-fluid align-self-center" alt=""></img></span><span class="align-self-center">Services</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#" tabindex="-1" aria-disabled="true"><span class="d-flex icons" style="margin-left:29px; margin-right:24px;"><img src="../static/medical.png" class="img-fluid align-self-center" alt=""></img></span><span class="align-self-center">Medical Records</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#" tabindex="-1" aria-disabled="true"><span class="d-flex icons" style="margin-left:29px; margin-right:24px;"><img src="../static/carewallet.png" class="img-fluid align-self-center" alt=""></img></span><span class="align-self-center">Care Wallet</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#" tabindex="-1" aria-disabled="true"><span class="d-flex icons" style="margin-left:29px; margin-right:24px;"><img src="../static/messages.png" class="img-fluid align-self-center" alt=""></img></span><span class="align-self-center">Messages</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#" tabindex="-1" aria-disabled="true"><span class="d-flex icons" style="margin-left:29px; margin-right:24px;"><img src="../static/resources.png" class="img-fluid align-self-center" alt=""></img></span><span class="align-self-center">Resources</span></a>
      </li>
    </ul>

    <!-- horizontal line -->
    <img src="../static/divider.png" alt="not loading" class="img-fluid" style="margin-top:36px;">

    <ul class="nav flex-column gap-4" style="margin-top:22px;">
      <li class="nav-item">
        <a class="nav-link" aria-current="page" href="#"><span class="d-flex icons" style="margin-left:29px; margin-right:24px;"><img src="../static/settings.png" class="img-fluid align-self-center" alt=""></img></span><span class="align-self-center">Account Settings</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#"><span class="d-flex icons" style="margin-left:29px; margin-right:24px;"><img src="../static/support.png" class="img-fluid align-self-center" alt=""></img></span><span class="align-self-center">Contact Support</span></a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#"><span class="d-flex icons" style="margin-left:29px; margin-right:24px;"><img src="../static/logout.png" class="img-fluid align-self-center" alt=""></img></span><span class="align-self-center">Logout</span></a>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'SidebarContent',
  data () {
    return {
      togglesidebar: true
    }
  },
  methods:
  {
    hidesidebar () {
      this.$emit('hidesidebar', !this.togglesidebar)
    }
  }
}
</script>
<style scoped>
.active
{
  background: #2A36A4;
  color: white !important;
}

.nav-link
{
  height: 56px;
  display: flex;
  color: #A0A0A0;
}
.nav-link:hover
{
  background: #2A36A4;
  color: white !important;
}
</style>
