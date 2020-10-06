<template>
  <div>
    <button v-show="loginIn">logout</button>
    <br>
    <svg-icon icon-class="device" />
    <br>
    username: <input v-model="loginFrom.username" type="text"> <br>
    password: <input v-model="loginFrom.password" type="password">
    <br>
    <button type="button" @click="login">submit</button>
  </div>
</template>

<script>
import { login, getInfo } from '@/api/user'
export default {
  data() {
    return {
      loginIn: true,
      loginFrom: {
        username: '',
        password: ''
      }
    }
  },
  mounted() {
    getInfo().then(result => {
      console.log(result)
    })
  },
  methods: {
    login() {
      login(this.loginFrom).then(result => {
        console.log('ss', result)
      })
    }
  }
}
</script>

<style lang="scss" scoped>

</style>
