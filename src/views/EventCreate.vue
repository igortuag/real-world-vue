<template>
  <div>
    <h1>Create am Evemt, {{ user.name }}</h1>
    <p>This event was created by {{ user.name }}</p>
    <p>There are {{ catLength }} categories</p>
    <ul>
      <li v-for="cat in categories" :key="cat">{{ cat }}</li>
    </ul>
  </div>
</template>

<script>
import { mapState, mapGetters } from 'vuex'

export default {
  computed: {
    ...mapGetters(['catLength']),
    ...mapState(['user', 'categories'])
  }
}
</script>

<style lang="scss" scoped></style>
