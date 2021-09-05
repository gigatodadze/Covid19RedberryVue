<template>

  <div>
    <div v-if="$auth.loggedIn">
      <!--      {{console.log($auth.user)}}-->
    </div>
    <div v-else>
      <form @submit.prevent="login">
        <h4>Login User</h4>
        <p>
          <label for="email" class="input-label">Email:</label>
          <input id="email" v-model="email" type="email" name="email" class="input">
          <label for="password" class="input-label">Passoword:</label>
          <input id="password" v-model="password" type="password" name="password" class="input">
        </p>
        <p>
          <button type="submit" value="Submit" class="button">Add Gin</button>
        </p>
      </form>
      <a href="#" @click.prevent="checkUser"> Login </a>

    </div>
  </div>

</template>

<script>

export default {

  methods: {
    login() {
      console.log(this.email);
      console.log(this.password);
      // console.log(this.$axios)
      this.$auth.loginWith('laravelSanctum',
        {
          data: {
            email:this.email,
            password: this.password,
          }
        },

        this.$axios.setToken('126|mS5qsEgJoUg8FfpRMVFxB5KzEu1BiLAe65bVuuQC', 'Bearer'),//სეტავს თოქენს და ავტორიზაცია წარმატებული ხდება
        // console.log(this.$auth.loggedIn),

      ).then(function (response) {
        this.axios.setToken(response.data.token, 'Bearer')//მაგრამ მანდ კიარა აქ უნდა ვსეტავდე რისპონსიდან წამოღებულ იუზერის ტოკენს, მაგრამ axios ს ვერ ხედავს იმიტორო ეს სხვა this ოა, ხოდა არ მუშაობს მოკლედ
      }   )
    },
    checkUser(){
      {{console.log(this.$auth.loggedIn)}}
    }
  }
}
</script>
