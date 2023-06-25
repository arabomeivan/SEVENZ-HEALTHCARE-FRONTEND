<template>
  <div>
    <div class="patient">
      Update Patient Medical Record
    </div>
    <div class="info">
      Click the tabs to view and edit patient medical details
    </div>

    <div class="medical-record">
      <!-- <div v-if="$apollo.loading">
        Loading...
      </div> -->
      <div>
        <ul>
          <li v-for="investor in investigations" :key="investor.id">
            {{ investor.title }}
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import gql from 'graphql-tag'

export default {
  name: 'IndexPage',
  layout: 'Dashboard',
  apollo: {
    investigations: {
      query: gql`
        query {
          investigations {
            id
            title
          }
        }
      `,
      prefetch: true,
      // Additional options for GET request
      fetchPolicy: 'network-only',
      context: {
        method: 'GET'
      }
    }
  },
  watch: {
    todos (newTodos) {
      console.log('Fetched todos:', newTodos)
    }
  }
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
