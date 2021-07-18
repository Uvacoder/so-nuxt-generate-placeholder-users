<template>
  <div>
    <p>Only 10 users are available, hence the second link should error</p>
    <nuxt-link to="/users/5">user 5</nuxt-link>
    <nuxt-link to="/users/11">user 11</nuxt-link>
    <div>Please visit a `/user/:id` path please</div>
  </div>
</template>
