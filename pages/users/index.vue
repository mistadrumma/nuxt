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
  async fetch({store}){
    if (store.getters['users/users'].length === 0){
      await store.dispatch('users/fetch')
    }

  },
  data: () => ({
  }),
  computed: {
    users(){
      return this.$store.getters['users/users']
    }
  },
  methods: {
      openUser(user) {
          this.$router.push('/users/' + user.id)
      }
  }
}
</script>
