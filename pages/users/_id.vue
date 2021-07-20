<template>
  <div>
    <div v-if="user">User name: {{ user.name }}</div>
    <div v-else-if="error">{{ error }}</div>
  </div>
</template>

<script>
export default {
  asyncData({ payload }) {
    if (payload && Object.entries(payload).length) return { user: payload }
    else return { error: 'This user does not exist' } // this will also can users going to `/users/`
  },
}
</script>
