<template>
    <main class="pt-5">
        <Search />
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
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';

main{
    background-color: $bg-page-color;
}

</style>