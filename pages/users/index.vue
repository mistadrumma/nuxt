<template>
  <section>
    <h1>Users Page</h1>
    <ul class="list-group">
      <div class="list-group">
        <li
          active-class="active"
          class="list-group-item list-group-item-action"
          v-for="user of users"
          :key="user.id"
          aria-current="true"
        >
          <a
            href="#"
            class="nav-link active"
            @click.prevent="openUser(user)"
          >
            {{user.name}}
          </a>
        </li>
      </div>
    </ul>
  </section>
</template>


<script>
export default {
  async asyncData({ $axios }) {
    const users = await $axios.$get('https://jsonplaceholder.typicode.com/users')
    return {users}
  },
  data: () => ({
    users: []
  }),
  methods: {
      openUser(user) {
          this.$router.push('/users/' + user.id)
      }
  }
}
</script>
