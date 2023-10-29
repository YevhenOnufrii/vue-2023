<template>
  <div class="container">
    <div class="img_box"><img :src="notebook.imgSrc" /></div>

    <div class="description_box">
      <a class="title" :href="notebook.link" target="_blank">{{ notebook.title }}</a>
      <p class="discount">
        Ваша економія <span> {{ notebook.discount }} грн</span>
      </p>
      <div class="old-price">{{ notebook.oldPrice }} грн</div>
      <div class="new-price">{{ notebook.price }} грн</div>
      <a class="link" :href="notebook.link" target="_blank">Купити</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ListItem',

  props: {
    notebook: {
      type: Object,
      default: () => ({}),
    },
  },
}
</script>

<style lang="css" scoped>
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

a {
  text-decoration: none;
  color: inherit;
}
.container {
  display: flex;
  gap: 16px;
  position: relative;
  width: 500px;
  padding: 16px;
  border: 1px solid transparent;
}

.container:hover {
  border: 1px solid red;
}

.img_box {
  width: 150px;
}

.img_box img {
  max-width: 100%;
  height: 100%;
}

.description_box {
  position: relative;
}
.title {
  color: #3d94df;
  text-decoration: underline;
  font-size: 18px;
}

.link {
  padding: 8px 16px;
  background-color: green;
  border-radius: 8px;
  position: absolute;
  bottom: 0;
  right: 0;
  color: white;
}

.discount span {
  color: red;
}

.discount {
  margin: 8px 0;
  color: gray;
  font-size: 14px;
}

.old-price {
  font-size: 14px;
  color: rgb(180, 172, 172);
  text-decoration: line-through;
}
.new-price {
  color: red;
  font-size: 20px;
}
</style>
