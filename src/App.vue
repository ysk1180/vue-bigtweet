<template>
  <div>
    <input type="radio" id="black" value="black" v-model="image">
    <label for="black"><img src="./assets/black.png"></label>
    <input type="radio" id="red" value="red" v-model="image">
    <label for="red"><img src="./assets/red.png"></label>

    <textarea v-model="msg" placeholder="ここに入力してください"></textarea>
    <p>
      {{ msg }}
    </p>
    <img :src="image_path(image)" />
  </div>
</template>

<script>
export default {
  data () {
    return {
      msg: '',
      image: 'black'
    }
  },
  methods: {
    image_path: function(value) {
      return require("./assets/" + value + ".png")
    }
  }
}
</script>

<style>
</style>
