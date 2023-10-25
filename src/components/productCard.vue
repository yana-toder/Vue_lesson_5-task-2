<template>
  <div class="container">
    <div class="img-wrap">
      <img :src="cardData.imgSrc" alt="image" class="img-wrap" />
    </div>
    <div class="content-wrap">
      <a :href="cardData.link" class="title">{{ cardData.title }}</a>
      <div class="economy">
        Ваша економія: <span>{{ cardData.discount }} ₴</span>
      </div>
      <div class="old-price">{{ cardData.oldPrice }} ₴</div>
      <div class="price">{{ cardData.price }} ₴</div>
      <button class="button" type="button">Купити</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductCard',

  props: {
    cardData: {
      type: Object,
      default: () => ({}),
    },
  },
}
</script>

<style lang="css" scoped>
.container {
  display: flex;
  height: 250px;
  margin-bottom: 30px;
}
.img-wrap {
  width: 200px;
  height: 200px;
  margin-right: 20px;
  align-self: center;
}
.content-wrap {
  padding: 10px;
}
.title {
  font-size: 20px;
  text-decoration: none;
  margin-bottom: 20px;
}
.economy {
  font-size: 12px;
  margin-bottom: 15px;
}
.economy span {
  color: red;
}
.old-price {
  color: gray;
  font-size: 14px;
  text-decoration-line: line-through;
  margin-bottom: 10px;
}
.price {
  color: red;
  font-size: 25px;
}

.button {
  background-color: rgb(62, 153, 62);
  color: #fff;
  font-size: 14px;
  padding: 5px 10px;
  margin-left: 300px;
  cursor: pointer;
}
.button:hover {
  background-color: rgb(28, 90, 28);
  transition: background-color 0.3s ease 0s;
}
</style>
