<template>
  <div class="aside">
    <div class="navigation">
      <ul class="navigation__list">
        <li class="navigation__item"><a href="#">Главная</a></li>
        <li class="navigation__item"><a href="#">Новости</a></li>
        <li class="navigation__item"><a href="#">Сообщения</a></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Aside',
  components: {

  }
}
</script>

<style scoped>

  aside {
    min-width: 100px;
    border-right: 3px solid var(--color-primary);
    text-align: left;
  }

  .navigation__list {
    list-style: none;
  }

  .navigation__list > .navigation__item {
    margin: 0 0 ;
    padding: 5px 10px;
  }

  .navigation__list > .navigation__item:hover {
    background: var(--color-primary-alpha);
  }

  .navigation__list > .navigation__item a {
    text-decoration: none;
    color: black;
  }

</style>