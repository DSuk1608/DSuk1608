<template>
  <nav>
<!--    only pages navigate NO COMPONENTS-->
    <NuxtLink to="/">test</NuxtLink>
    <NuxtLink to="/PerUser">UserInfo</NuxtLink>
    <NuxtLink to="/Users">Users</NuxtLink>
  </nav>
</template>

<script>
export default {
  name: "NavBar"
}
</script>

<style scoped>

</style>
