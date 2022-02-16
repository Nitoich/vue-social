<template>
  <div class="content">
    <div class="news">
      <h1 class="title center">Новости</h1>
      <ul class="news__list">
        <Post :image="'https://megatopof.ru/files/2014/krutoy-chel-3.jpg'" />
        <Post :image="'https://otvet.imgsmail.ru/download/37511698_f5d0881286392e75320b4ff203e9b9ad_800.jpg'" />
        <Post :image="'https://cdn.trinixy.ru/pics4/20100204/photos_of_guy_from_russian_social_network_01.jpg'" />
        <Post :image="'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQUKRrA-M10ii6C73vyAMJmT59OZeScDLl_2Q&usqp=CAU'" />
      </ul>
    </div>
  </div>
</template>

<script>

  import Post from '@/components/post';

  export default {
    name: 'MainContent',
    components: {
      Post
    }
  }
</script>

<style scoped>

  .main .content {
    flex: 1;
    box-sizing: border-box;
    padding-left: 10px;
  }

  .title {
    position: relative;
  }

  .title::after {
    content: " ";
    position: absolute;
    width: 30%;
    height: 2px;
    background: var(--color-primary-alpha);
    bottom: -2px;
    left: calc(50% - 15%)
  }

  .title.center {
    text-align: center;
  }

  .news__list {
    list-style: none;
  }

  @media screen and (max-width: 768px) {
    .main .content {
      padding: 0;
    }
  }

</style>