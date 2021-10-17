<template>
  <div id="nav">
    <router-link :class="{active: $route.name === 'Home'}" to="/">Home</router-link>
    <router-link :class="{active: $route.name === 'Cart'}" to="/cart">Cart</router-link>
  </div>
  <router-view />
</template>

<style lang="scss">
@font-face {
  font-family: "cotham_sansregular";
  src: url("./assets/typeface/cothamsans-webfont.woff2") format("woff2"),
    url("./assets/typeface/cothamsans-webfont.woff") format("woff");
  font-weight: normal;
  font-style: normal;
}

#app {
  font-family: cotham_sansregular, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

html,
body {
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}

body {
  background-color: #F1F7ED;
}

#nav {
  padding: 1rem;
  background-color: #243e36;
  width: 100%;
  height: 2rem;
  display: flex;
  justify-content: center;

  a {
    color: #e0eec6;
    text-decoration: none;
    font-size: 1.6rem;
    margin-right: 1.6rem;
    padding: 0.2rem;

    &.active, &:active, &:hover {
        color: rgb(194, 168, 62);
    }
  }
}
</style>
