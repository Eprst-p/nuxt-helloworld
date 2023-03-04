<template>
  <div>
    <h1>{{ message }}</h1>
  </div>

</template>

<script>
export default {
  name: 'IndexPage',
  async asyncData({$http}) {
    const message = await $http.$get('/api/hello')
    return {
      message
    }
  }
}
</script>

<style>
h1 {
  margin: 20px auto
}
</style>
