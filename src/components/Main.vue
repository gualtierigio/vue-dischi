<template>
    <main class="pt-5">
        <Album />
    </main>
</template>

<script>
import Album from './Album.vue'

export default {
    name: 'Main',
    components: {
    Album,
  },
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';

main{
    background-color: $bg-page-color;
}

</style>