<template>
    <form class="d-flex">
        <div>
            <input class="form-control" type="text" placeholder="chiedi cose">
        </div>
        <div>
            <button class="btn btn-outline-light">Find it</button>
        </div>
        <div>
            <button class="btn btn-outline-dark">Reset</button>
        </div>
    </form>
</template>

<script>

export default {
    name: 'Search',
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