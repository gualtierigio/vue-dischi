<template>
    <div class="card">
        <img src="https://img.discogs.com/vknPDdrqRbT92pNRX0W4I5N91jg=/fit-in/300x300/filters:strip_icc():format(jpeg):mode_rgb():quality(40)/discogs-images/R-1246953-1448927086-6590.jpeg.jpg" alt="">
        <div class="description">
            <h3>bla bla bla</h3>
            <p>dgnuifebgudbgujidgi</p>
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
    height: 300px;
    width: calc(100% / 5 - 40px);
    background-color: $base-color;
    margin: 20px;
}

img{
    padding: 10%;
}

.description{
    padding: 0 10%;
    text-align: center;
    h3{
    color: white;
    }
    p{
        font-size: 0.8rem;
        color: rgb(65, 65, 65);
    }
}


</style>