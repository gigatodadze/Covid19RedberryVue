<!--<template>-->
<!--  <div class="country-list-row">-->
<!--    <tr v-for="country in countries">-->
<!--      <td>{{ country.id }}</td>-->
<!--      <td>{{ country.code }}</td>-->
<!--      <td>{{ country.name }}</td>-->
<!--    </tr>-->
<!--  </div>-->
<!--</template>-->

<!--<script>-->
<!--import axios from 'axios'-->
<!--export default {-->
<!--  name: 'country-list-row',-->
<!--  mounted: function () {-->
<!--    this.getCountries()-->
<!--    console.log('mounted: got here')-->
<!--  },-->
<!--  data: function () {-->
<!--    return {-->
<!--      message: 'Country List Row',-->
<!--      countries: []-->
<!--    }-->
<!--  },-->
<!--  methods: {-->
<!--    getCountries: function () {-->
<!--      const url = 'http://localhost:8000/api/countries/'-->
<!--      axios.get(url, {-->
<!--        dataType: 'json',-->
<!--        headers: {-->
<!--          'Accept': 'application/json',-->
<!--          'Content-Type': 'application/json'-->
<!--        },-->
<!--        mode: 'no-cors',-->
<!--        credentials: 'include'-->
<!--      })-->
<!--        .then(function (response) {-->
<!--          console.log(JSON.stringify(response.data))-->
<!--          this.countries = JSON.stringify(response.data)-->
<!--        })-->
<!--        .catch(function (error) {-->
<!--          console.log(error)-->
<!--        })-->
<!--    }-->
<!--  }-->
<!--}-->
<!--</script>-->
