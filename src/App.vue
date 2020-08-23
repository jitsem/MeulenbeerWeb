<template>
  <div id="app">
    <router-view/>
    <footer>&copy; 2020 <a href="https://www.jitsem.be">jitsem</a></footer>
  </div>
</template>

<style>
* {
  margin: 0;
  padding: 0;
}

html {
  min-height: 100%;
  background-color: #efefef;
  line-height: 1.4;
}
#app {
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  width: 80%;
  margin: auto;
}

footer {
    background-color: #2aa9f4;
    color: #e3e3e3;
    position: absolute;
    left: 0;
    bottom: 0;
    height: 25;
    width: 100%;
    overflow: hidden;
    text-align: center;
}

footer a {
  text-decoration: none;
  color: #e3e3e3;
}

footer a:hover {
  color: #fee715;
}

</style>
