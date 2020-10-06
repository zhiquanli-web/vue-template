<template>
  <div>
    <button v-show="loginIn">logout</button>
    <br>
    <svg-icon icon-class="device" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      loginIn: true
    }
  },
  methods: {

  }
}
</script>

<style lang="scss" scoped>

</style>
