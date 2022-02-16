<template>
  <div id="app">
    <Mainheader />

    <main class="main">
      <div class="wrapper flex">
        <Aside />
        <MainContent />
      </div>
    </main>

  </div>
</template>

<script>

import Mainheader from "@/templates/header";
import Aside from "@/templates/aside";
import MainContent from "@/templates/maincontent";

export default {
  name: 'App',
  components: {
    Mainheader,
    Aside,
    MainContent
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

:root {
  --color-primary: #4796b4;
  --color-primary-alpha: #4796b455;
}

* {
  margin: 0;
  padding: 0;
}

.flex {
  display: flex;
}

.flex.f-center {
  justify-content: center;
  align-items: center;
}

.flex.f-jcc {
  justify-content: center;
}

.flex.f-aic {
  align-items: center;
}

.flex.f-jcsb {
  justify-content: space-between;
}

.flex.f-column {
  flex-direction: column;
}

.wrapper {
  width: 60%;
  margin: 0 auto;
}

.avatar {
  width: 40px;
  height: 40px;
  overflow: hidden;
  border-radius: 50%;
  border: 3px solid black;
}

.avatar > img {
  width: 40px;
  height: auto;
}

@media screen and (max-width: 1024px) {
  .wrapper {
    width: 80%;
  }
}

@media screen and (max-width:  768px) {
  .wrapper {
    width: 100%;
    box-sizing: border-box;
    padding: 0 5px;
  }

  .aside {
    display: none;
  }
}

</style>
