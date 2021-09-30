<template>
    <form class="d-flex" v-on:submit.prevent>
        <div>
            <input v-model.trim="needle" class="form-control" type="text" placeholder="chiedi cose">
        </div>
        <div>
            <button @click.prevent="$emit('search', needle)" class="btn btn-outline-light" type="submit">Find it</button>
        </div>
        <div>
            <button class="btn btn-outline-dark" type="reset">Reset</button>
        </div>
    </form>
</template>

<script>

export default {
    name: 'Search',
    data: function() {
        return{
            needle: '',
        }
    },
    methods: {
        sendInputSearch(neeadle){
            console.log(neeadle);
        }
    }
}

</script>

<style lang="scss" scoped>
@import '../style/variables.scss';
@import '../style/general.scss';

form{
    min-width: 400px;
    margin: 50px 50px;
    justify-content: center;
}

</style>