<template>
  <div>
    <div class="patient">
      Update Patient Medical Record
    </div>
    <div class="info">
      Click the tabs to view and edit patient medical details
    </div>

    <div class="medical-record" />
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  layout: 'Dashboard'
}
</script>
<style scoped>
.patient
{
  color: #382F90;
  font-size: 32px;
  font-family: 'Open sans';
  font-weight: bold;
  margin-top: 49px;
}
.info
{
color:  #9FA2B4;
font-family: 'Open Sans';
margin-top: 13px;
}

</style>
