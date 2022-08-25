<template>
<div>
  <h1>Hello, nuxt-app</h1>
</div>
</template>

<script>
import auth from "@/middleware/auth";

export default {
  middleware: [auth],
  name: 'IndexPage'
}
</script>
