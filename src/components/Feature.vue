<template>
  <!-- <div :class="`feature ${alignment}`"> -->
  <div :class="`feature ${alignment}`">
    <div class="img">
      <img :src="require(`../assets/${feature.img}`)" alt="" />
    </div>
    <div class="txt">
      <h2 v-html="headline"></h2>
      <p>
        {{ feature.text }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Feature",
  props: {
    // align: String,
    center: Boolean,
    feature: Object,
  },
  computed: {
    alignment: function () {
      //   return this.center ? "center" : this.align === "left" ? "left" : "right";
      return this.center ? "center" : "";
    },
    headline: function () {
      return this.feature.title.replace(
        this.feature.emph,
        `<span class="emph">${this.feature.emph}</span>`
      );
    },
  },
};
</script>

<style scoped>
.feature {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-top: 120px;
}
.txt {
  display: flex;
  flex-direction: column;
  gap: 20px;
  flex: 0 1 auto;
  align-items: center;
}
.txt h2 {
  max-width: clamp(268px, 40vw, 520px);
  font-size: clamp(25px, 3vw, 40px);
  line-height: 117%;
  letter-spacing: -0.05em;
  color: var(--grey-600);
}
.txt p {
  max-width: clamp(335px, 40vw, 520px);
  color: var(--grey-400);
  font-size: clamp(16px, 2.5vw, 18px);
  line-height: 185.6%;
  letter-spacing: -0.03em;
}
/* .txt .emph {
  color: var(--primary-400);
  font-style: italic;
} */
.img {
  min-width: 300px;
  max-width: 400px;
  flex: 0 1 auto;
}
img {
  width: 100%;
}
/* .feature.right .txt {
  order: -1;
} */

.feature:nth-child(odd) .txt {
  order: -1;
}

.feature.center {
  flex-direction: column;
  align-items: center;
  gap: 30px;
  text-align: center;
}

.feature.center .txt h2 {
  max-width: clamp(268px, 45vw, 570px);
}
.feature.center .txt p {
  max-width: clamp(268px, 55vw, 750px);
}
.feature.center .img {
  margin-top: 40px;
}
@media screen and (max-width: 768px) {
  .feature {
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 50px;
    padding-top: 70px;
  }
  .txt {
    order: -1;
    flex-direction: column;
    gap: 20px;
    flex: 0 1 auto;
  }

  .img {
    min-width: 150px;
    max-width: 280px;
    flex: 0 1 auto;
  }
}
</style>
