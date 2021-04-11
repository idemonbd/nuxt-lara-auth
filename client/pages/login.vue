<template>
  <div>
    <div class="col-md-4">
      <button v-if="!$auth.loggedIn" @click.prevent="login" class="btn btn-primary mt-2">Login</button>
    </div>
  </div>
</template>

<script>
export default {

  methods: {
    login() {
      this.$auth.loginWith('laravelSanctum', {
        data: {
          email :'user@mail.com',
          password:'user@mail.com'
        }
      })
    },
  },
};
</script>

<style>
</style>