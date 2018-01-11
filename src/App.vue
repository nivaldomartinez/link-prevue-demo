<template>
  <div id="app">
    <h1>Link Prevue</h1>
    <div class="url-group">
      <input type="text" name="urlfield" v-model="url" placeholder="Type an url" @keyup:enter="changeUrl" @blur="changeUrl">
      <a href="#">Prevue</a>
    </div>
    <link-prevue :url="url"></link-prevue>
    <footer>
      <a href="https://github.com/nivaldomartinez/link-prevue" target="_blank">View on github</a>
    </footer>
  </div>
</template>

<script>
import LinkPrevue from 'link-prevue'

export default {
  name: 'app',
  components: {
    LinkPrevue
  },
  data () {
    return {
      url: null
    }
  },
  methods: {
    changeUrl: function(event) {
      this.url = event.target.value
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Hind+Siliguri:400,600');

body {
  background-color: #fdf1ec;
}

h1 {
  font-family: 'Hind Siliguri', sans-serif;
  font-size: 40px;
  color: #686868;
}

footer {
    padding-top: 30px;
}

footer a {
  font-family: 'Hind Siliguri', sans-serif;
  font-size: 15px;
  text-decoration: none !important;
  color: #8d8d8d;
}
#app {
  position: fixed;
  width: 20%;
  z-index: 2;
  top: 25%;
  left: 50%;
  margin-top: -10%;
  margin-left: -10%;
}

.url-group {
    width: 400px;
    margin-bottom: 10px;
    overflow: hidden;
}

.url-group input[type="text"] {
  height: 40px;
  border: none;
  padding: 1.5px;
  padding-left: 10px;
  padding-right: 10px;
  border-radius: 10px 0 0 10px;
  border-color: transparent;
  width: 72.5%;
  display: inline;
  margin: 0;
  float: left;
  color: #8d8d8d;
  font-family: 'Hind Siliguri', sans-serif;
  font-size: 15px;
}

.url-group input[type="text"]:focus {
    outline: none;
}

.url-group a {
  float: right;
  border-radius: 0 10px 10px 0;
  font-family: 'Hind Siliguri', sans-serif;
  font-size: 14px;
  letter-spacing: 0.1em;
  color: #ffffff;
  background-color: #ffa9be;
  padding: 10px 20px 10px 20px;
  text-align: center;
  display: inline-block;
  text-decoration: none !important;
  -webkit-transition: all 0.2s ease-in-out;
  -moz-transition: all 0.2s ease-in-out;
  -ms-transition: all 0.2s ease-in-out;
  -o-transition: all 0.2s ease-in-out;
  transition: all 0.2s ease-in-out;
}

.url-group a:hover {
  background-color: #ff8fab;
}
</style>
