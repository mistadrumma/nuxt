<template>
  <section>
    <h1>Users Page</h1>
    <ul class="list-group">
      <div class="list-group">
        <li
          active-class="active"
          class="list-group-item list-group-item-action"
          v-for="user of 5"
          :key="user"
          aria-current="true"
        >
          <a
            href="#"
            class="nav-link active"
            @click.prevent="openUser(user)"
          >
            User {{user}}
          </a>
        </li>
      </div>
    </ul>
  </section>
</template>


<script>
export default {
    methods: {
        openUser(user) {
            this.$router.push('/users/' + user)
        }
    }
}
</script>