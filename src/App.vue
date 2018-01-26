<template>
  <div id="app">
    <div class="nav-bar">
      <ul class="nav-bar-list">
        <li class="nav-bar-item">Home</li>
        <li class="nav-bar-item">Cats</li>
        <li class="nav-bar-item">Adoptions</li>
      </ul>
    </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {}

* {
  margin: 0;
  padding: 0;
}

.nav-bar {
  background-color: #dedede;
  width: 1920px;
  height: 100px;
  padding: 20px;
}

.nav-bar-list {
  list-style: none;
  margin: 20px;
}

.nav-bar-item {
  float: left;
  margin: 5px;
  height: 40px;
  width: 120px;
  font-size: 26px;
  text-align: center;
  background-color: pink;
}
</style>
