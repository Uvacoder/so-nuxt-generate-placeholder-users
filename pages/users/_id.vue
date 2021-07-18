<template>
  <div>User name: {{ user.name }}</div>
</template>

<script>
export default {
  asyncData({ payload, redirect }) {
    if (payload && Object.entries(payload).length) return { user: payload }
    else redirect({ name: 'no-user' }) // this will also can users going to `/users/`
  },
}
</script>
