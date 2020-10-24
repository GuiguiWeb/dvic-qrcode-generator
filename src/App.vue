<template>
  <div id="app">
    <div class="app__head">
      <img src="@/assets/logo.svg" alt="">
      <h1>QR CODE GENERATOR</h1>
    </div>
    <div class="app__form">
      <input type="text" name="" v-model="config.value">
    </div>
    <div class="app__qrcode">
      <div class="box">
        <vue-q-art :config="config"></vue-q-art>
      </div>
    </div>
  </div>
</template>

<script>
import VueQArt from 'vue-qart'

export default {
  name: 'App',
  data () {
    return {
      config: {
        value: 'http://dvic.devinci.fr/',
        imagePath: './logo.svg',
        filter: 'color'
      }
    }
  },
  components: {
    VueQArt
  }
}
</script>

<style lang="scss">
body {
  background-color: #222f3e;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 20px;
}

.app__head {
  text-align: center;

  h1 {
    color: #f5f6fa;
    margin-top: 0;
  }

  img {
    width: 300px;
    height: auto;
    margin-bottom: 0;
  }
}

.app__form {
  text-align: center;

  input {
    outline: 0;
    background: #40739e;
    border: none;
    border-radius: 2px;
    margin: 0 0 15px;
    min-width: 300px;
    padding: 15px;
    box-sizing: border-box;
    font-size: 14px;
  }
}

.app__qrcode {
  display: flex;
  justify-content: center;
}

.box {
  background-color: #f5f6fa;
  border-radius: 2px;
  width: 300px;
  height: 300px;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
