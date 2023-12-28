<template>
    <ul>
    <li>{{data.response}}</li>
    </ul>
</template>

<script>
import axios from 'axios';


export default {
//   data() {
//     return {
//       responseData: null,
//       error: null
//     };
//   },
  mounted() {
    // Gantilah URL dengan endpoint API yang sesuai
    const apiUrl = 'http://localhost:8080/semua';


    axios.get(apiUrl)
      .then(response => {
        // Handle response data di sini
        this.responseData = response.data;
      })
      .catch(error => {
        // Handle error di sini
        this.error = error;
      });
  }
}


</script>
