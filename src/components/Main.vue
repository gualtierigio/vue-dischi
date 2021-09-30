<template>
    <main class="pt-5">
        <Search @search="searchInCaracters"/>
        <Album />
    </main>
</template>

<script>
import Album from './Album.vue';
import Search from './Search.vue';

export default {
    name: 'Main',
    components: {
    Album,
    Search
  },
  data() {
      return {
          needle: ''
      }
  },
  methods: {
      searchInCaracters(needle) {
          this.needle = needle;
      }
  },
  computed: {
      filterCharactersList() {
          const newCharactersList = this.searchInCaracters.filter(
              (element) => {
                  element.name.toLowerCase().includes(this.needle.toLowerCase())
              }
          );

          return newCharactersList;
      }
  }
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';

main{
    background-color: $bg-page-color;
}

</style>