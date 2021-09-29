<template>
    <main class="pt-5">
        <div class="container">
            <div class="row">
                <div class="col-12 d-flex flex-wrap">
                    <Album />
                    <Album />
                    <Album />
                    <Album />
                    <Album />
                    <Album />
                    <Album />
                    <Album />
                    <Album />
                    <Album />
                </div>
            </div>
        </div>
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
    height: calc(100vh - 100px);
    background-color: $bg-page-color;
}

</style>