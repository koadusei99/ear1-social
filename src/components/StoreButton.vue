<template>
  <a href="" :class="`${color} link btn`">
    <div class="icon">
      <img :src="require(`../assets/${store}.svg`)" alt="" />
    </div>
    <div class="txt">
      <p class="get">Get it on</p>
      <p class="store">{{ txt }}</p>
    </div>
  </a>
</template>

<script>
export default {
  name: "StoreButton",
  props: {
    store: String,
    color: String,
  },
  computed: {
    txt: function () {
      return this.store === "appstore" ? "App Store" : "Google Play";
    },
  },
};
</script>

<style scoped>
.btn {
  padding: 15px 20px;
  display: flex;
  max-width: 180px;
  gap: 12px;
  align-items: center;
  height: fit-content;
  border-radius: 5px;
  text-decoration: none;
}

.green {
  background-color: var(--primary-400);
  transition: all 200ms ease-in;
}
.green:hover {
  background-color: var(--primary-300);
}
.dark {
  background-color: var(--grey-600);
  transition: all 200ms ease-in;
}
.dark:hover {
  background-color: var(--grey-500);
}
.txt {
  color: white;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
.get {
  font-size: 12px;
  font-weight: 500;
}
.store {
  font-size: 18px;
  font-weight: 600;
}
@media screen and (max-width: 768px) {
  .btn {
    width: 100%;
  }
}
</style>
