<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <!-- 注意这里要加上mode="out-in"，防止出现闪屏 -->
    <transition name="router" mode="out-in">
      <router-view key="$route.fullPath" />
    </transition>
  </div>
</template>
<style lang="scss">
.router-enter {
  transform: translateX(20px);
  opacity: 0;
}
.router-enter-active {
  transition: all 0.3s ease;
}
.router-enter-to {
  transform: translateX(0px);
  opacity: 1;
}
.router-leave {
  transform: translateX(0px);
  opacity: 1;
}
.router-leave-active {
  transition: all 0.3s ease;
}
.router-leave-to {
  transform: translateX(20px);
  opacity: 0;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  overflow-x: hidden;
}

</style>
