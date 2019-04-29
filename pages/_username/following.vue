<template>
  <div>
    <h1>Users following {{ username }}</h1>
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
          content: ` You are watching users that are following ${this.username}`
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
