<template>
  <header class="header">
    <div class="wrapper flex f-jcsb f-aic">
      <button class="burger-nav-btn" :class="{active:isActive}" @click="showMobileMenu">
        <span></span>
      </button>
      <div class="header__logo">
        <h1>Social</h1>
      </div>
      <div class="header__user flex f-aic">
        <div class="header__username">
          Nitoich
        </div>
        <div class="header__useravatar flex f-center">
          <img src="https://sun9-86.userapi.com/sun9-81/impf/c624617/v624617325/1424c/8ZRNT_7oKUM.jpg?size=460x480&quality=96&sign=17ac077591cbb92163f9d94f7c7bd873&type=album" alt="avatar">
        </div>
      </div>
    </div>

    <div class="aside-mobile" :class="{active:isActive}">

    </div>
  </header>
</template>

<script>
  export default {
    name: "v-header",
    data() {
      return {
        isActive: false
      }
    },
    methods: {
      showMobileMenu() {
        if (this.isActive) { this.isActive = false } else {this.isActive = true}
      }
    }
  }
</script>

<style scoped>

  .aside-mobile {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background: #000000AA;
    z-index: 2;
    transition: 0.5s;
    transform: translateX(-100%);
    display: none;
  }

  .aside-mobile.active {
    transform: translateX(0);
  }

  header.header {
    background: var(--color-primary);
    padding: 10px 0;
    margin-bottom: 20px;
  }

  .header__useravatar {
    width: 40px;
    height: 40px;
    overflow: hidden;
    border-radius: 50%;
    border: 3px solid black;
    margin-left: 20px;
  }

  .burger-nav-btn {
    display: none;
    width: 50px;
    height: 50px;
    position: relative;
    border: none;
    z-index: 3;
  }

  .burger-nav-btn > span,
  .burger-nav-btn > span:after,
  .burger-nav-btn > span:before{
    content: "";
    position: absolute;
    display: block;
    height: 2px;
    width: 40px;
    background: #000;
    top: 24px;
    left: 5px;
    transition: 0.3s;
  }

  .burger-nav-btn.active span:before {
    transform: translateY(-10px) rotate(90deg);
  }

  .burger-nav-btn.active span{
    transform: rotate(45deg);
  }



  .burger-nav-btn.active span:after {
    opacity: 0;
  }

  .burger-nav-btn > span:after {
    top: -10px;
    left: 0;
  }

  .burger-nav-btn > span:before {
    top: 10px;
    left: 0;
  }

  .header__useravatar > img {
    width: 40px;
    height: auto;
  }

  @media screen and (max-width: 768px) {
    header.header {
      position: fixed;
      width: 100%;
      z-index: 1;
    }

    .aside-mobile {
      display: block;
    }

    .burger-nav-btn {
      display: block;
    }

    .header__user {
      display: none;
    }
  }
</style>