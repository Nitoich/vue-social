<template>
  <li class="news__item">
    <div class="news__header flex f-jcsb f-aic">
      <div class="news__author">
        <div class="author flex f-aic">
          <div class="author__avatar avatar">
            <img src="https://sun9-86.userapi.com/sun9-81/impf/c624617/v624617325/1424c/8ZRNT_7oKUM.jpg?size=460x480&quality=96&sign=17ac077591cbb92163f9d94f7c7bd873&type=album" alt="avatar">
          </div>
          <div class="author__name">Nitoich</div>
        </div>
      </div>

      <div class="news__date">
        1987-03-02
      </div>
    </div>

    <div class="news__image flex f-center">
      <img :src='image' alt="IMAGE">
    </div>

    <div class="news__footer">
      <div class="news__text">
        Lorem Ipsum - это текст-"рыба", часто используемый в печати и вэб-дизайне. Lorem Ipsum является стандартной "рыбой" для текстов на латинице с начала XVI века. В то время некий безымянный печатник создал большую коллекцию размеров и форм шрифтов, используя Lorem Ipsum для распечатки образцов. Lorem Ipsum не только успешно пережил без заметных изменений пять веков, но и перешагнул в электронный дизайн. Его популяризации в новое время послужили публикация листов Letraset с образцами Lorem Ipsum в 60-х годах и, в более недавнее время, программы электронной вёрстки типа Aldus PageMaker, в шаблонах которых используется Lorem Ipsum.
      </div>

      <div class="news__stat">
        <button class="btn-like">4 | Like</button>
      </div>
    </div>
  </li>
</template>

<script>
export default {
  name: 'Post',
  props: {
    image: String
  }
}
</script>

<style scoped>

  .author__name {
    margin-left: 10px;
  }

  .news__item {
    width: 100%;
    height: auto;
    border: 1px solid #23232355;
    margin: 10px 0;
    box-sizing: border-box;
    padding: 20px;
  }

  .btn-like {
    background: transparent;
    border: 2px solid var(--color-primary);
    padding: 5px 10px;
    border-radius: 20px;
    cursor: pointer;
  }

  .btn-like:hover {
    background: var(--color-primary-alpha);
  }

  .news__stat {
    margin-top: 10px;
  }

  .news__text {
    line-height: 20px;
  }

  .news__item > * {
    margin: 10px 0;
  }

  .news__image > img {
    width: 100%;
  }
</style>