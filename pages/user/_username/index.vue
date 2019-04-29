<template>
  <div>
    <h1>User {{ username }}</h1>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: `User: ${this.username}`,
      meta: [
        {
          hid: 'description',
          name: 'description',
          content: ` You are watching user ${this.username}`
        }
      ]
    }
  },
  computed: {
    username() {
      return this.$route.params.username
    }
  }
}
</script>
