<template>
  <div>
    <NavBar />
    <main>
      <div class="container">
        <Nuxt />
      </div>
    </main>
  </div>
</template>

<script>
import Navbar from "@/components/NavBar";
export default {
  components: {
    Navbar,
  },
};
</script>