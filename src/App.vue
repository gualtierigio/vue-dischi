<template>
  <div>
    <Header />
    <Main />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import axios from "axios"

export default {
  name: "App",
  components: {
    Header,
    Main,
  },
  data() {
    return {
      albums: [],
    }
  },
  mounted() {
    axios.get('https://flynn.boolean.careers/exercises/api/array/music')
    .then((resp) => {
      this.albums = resp.data.response;
    })
  }
};
</script>

<style lang="scss">
@import 'style/general.scss';
@import 'style/variables.scss';

</style>
