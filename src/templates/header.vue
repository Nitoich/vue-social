<template>
  <header class="header">
    <div class="wrapper flex f-jcsb f-aic">
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
  </header>
</template>

<script>

</script>

<style scoped>
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



.header__useravatar > img {
  width: 40px;
  height: auto;
}
</style>