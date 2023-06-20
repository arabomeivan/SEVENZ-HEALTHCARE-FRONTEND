<template lang="">
  <div>
    <nav class="navbar fixed">
      <div class="container-fluid justify-content-end">
        <div class="d-flex justify-content-between gap-4">
          <div class="align-self-center togglesidebar">
            <i class="fa-solid fa-arrow-right" @click="hidesidebar" />
          </div>
          <div class="align-self-center">
            <nuxt-link to="#">
              Take a tour
            </nuxt-link>
          </div>
          <div class="align-self-center">
            <button type="button" class="btn">
              <img class="img-fluid" src="../static/message.png" alt="">
            </button>
          </div>

          <div class="align-self-center">
            <button type="button" class="btn">
              <img class="img-fluid" src="../static/bell.png" alt="">
            </button>
          </div>

          <div class="align-self-center">
            <img class="img-fluid profilepic rounded-circle" src="../assets/profilepic.jpg" alt="not found">
          </div>
          </button>
        </div>
      </div>
    </nav>
  </div>
</template>
<script>
export default {
  name: 'NavBar',
  data () {
    return {
      togglesidebar: false
    }
  },
  methods:
  {
    hidesidebar () {
      this.togglesidebar = !this.togglesidebar
      this.$emit('hidesidebar', this.togglesidebar)
    }
  }
}
</script>
<style scoped>
.navbar {
  background: transparent;
  color: #382f9099 !important;
  font-size: 18px;
  font-family: 'Open Sans';
  font-weight: bold;
  font-size: 18px;
}
a
{
  color: #382f9099;
  text-decoration: none;
}
.btn {
  box-shadow: none;
}
.profilepic
{
  width: 50px;
  height: 50px;
}
</style>
