<template>
  <section class="hero">
    <div class="bubble">
      <img src="../assets/Davido.png" alt="" />
      <img src="../assets/Prosper.png" alt="" />
      <img src="../assets/Shola.png" alt="" />
      <img src="../assets/Moe.png" alt="" />
    </div>
    <div class="content">
      <h1>Connect with professionals in your field without getting aired.</h1>
      <p>
        For a small fee, ear1 allows you to get in touch with professionals in
        your field and build quality relationships with them.
      </p>

      <div class="store-btns">
        <StoreButton color="green" store="appstore" />
        <StoreButton color="green" store="playstore" />
      </div>
    </div>
  </section>
</template>

<script>
import StoreButton from "./StoreButton.vue";
export default {
  name: "Hero",
  components: { StoreButton },
};
</script>

<style scoped>
.hero {
  position: relative;
  padding-top: 50px;
  padding-bottom: 200px;
  padding-inline: clamp(30px, 3vw, 200px);
}
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 40px;
  max-width: 745px;
  text-align: center;
  margin: 0 auto;
  position: relative;
  z-index: 2;
}

.content h1 {
  max-width: clamp(314px, 50vw, 750px);
  font-weight: 700;
  line-height: 118%;
  letter-spacing: -0.05em;
  font-size: clamp(30px, 3.5vw, 50px);
  color: var(--grey-600);
}
.content p {
  width: clamp(325px, 55vw, 563px);
  font-size: clamp(18px, 2vw, 20px);
  line-height: 165.6%;
  letter-spacing: -0.03em;
  color: var(--grey-500);
}
.store-btns {
  margin-top: 25px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}
.bubble img {
  width: 90px;
  position: absolute;
  z-index: 1;
}
.bubble img:first-of-type {
  top: 130px;
  left: min(150px, 10%);
}
.bubble img:nth-of-type(2) {
  top: 120px;
  right: min(150px, 10%);
}
.bubble img:nth-of-type(3) {
  bottom: 90px;
  left: min(270px, 22%);
}
.bubble img:last-of-type {
  bottom: 105px;
  right: min(270px, 22%);
}

@media screen and (max-width: 960px) {
  .bubble img {
    width: 65px;
  }
}
@media screen and (max-width: 768px) {
  .bubble img {
    width: 44px;
  }
  .bubble img:first-of-type {
    top: 12px;
    left: 25px;
  }
  .bubble img:nth-of-type(2) {
    top: 12px;
    right: 25px;
  }
  .bubble img:nth-of-type(3) {
    bottom: 95px;
    left: 35px;
  }
  .bubble img:last-of-type {
    bottom: 115px;
    right: 34px;
  }
}
</style>
