<template>
<div>
  <button v-show="loginIn">logout</button>
</div>
</template>

<script>
export default {
  data() {
    return {
      loginIn: true
    }
  },
}
</script>

<style lang="scss" scoped>

</style>
