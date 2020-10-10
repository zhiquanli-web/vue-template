<template>
  <div>
    <button v-show="loginIn">logout</button>
    <br>
    <svg-icon icon-class="device" />
    <br>
    username: <input v-model="loginForm.username" type="text"> <br>
    password: <input v-model="loginForm.password" type="password">
    <br>
    <button type="button" @click="login">submit</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      loginIn: false,
      loginForm: {
        username: '',
        password: ''
      }
    }
  },
  methods: {
    login() {
      console.log(this.loginForm)
      this.$store
        .dispatch('user/login', this.loginForm)
        .then(() => {
          this.$router.push({ path: '/home' })
          this.loading = false
        })
        .catch(() => {
          this.loading = false
        })
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
