<template>
  <div>
    <h1>Home</h1>
    <p>{{ message }}</p>
    <input v-model="newMessage" />
    <button @click="updateMessage">Update Message</button>
  </div>
</template>

<script>
import { mapState, mapActions } from 'vuex'

export default {
  data() {
    return {
      newMessage: ''
    }
  },
  computed: {
    ...mapState(['message'])
  },
  methods: {
    ...mapActions(['updateMessage'])
  }
}
</script>
