<template>
    <div class="container">
        <div class="row">
            <div class="col-6 col-md-4 col-lg-3" v-for="(album, index) in albums" :key="index">
                <div class="card">
                    <img :src="album.poster" :alt="album.author">
                    <div class="description">
                        <p class="title">{{album.title}}</p>
                        <p>{{album.author}} <br>{{album.year}}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import axios from "axios";

export default {
    name: 'Album',

    data() {
    return {
      albums: [],
    }
  },

    mounted() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((resp) => {
        this.albums = resp.data.response;
        console.log(this.albums);
    })
  }
}

</script>

<style lang="scss" scoped>
@import '../style/variables.scss';

.card{
    height: 350px;
    background-color: $base-color;
    margin: 20px;
}

img{
    padding: 10% 10% 5% 10%;
}

.description{
    padding: 0 10%;
    text-align: center;
    p.title{
    color: white;
    font-size: 1.3rem;
    font-weight: bold;
    line-height: 22px;
    }
    p{
        font-size: 0.8rem;
        color: rgb(65, 65, 65);
    }
}


</style>