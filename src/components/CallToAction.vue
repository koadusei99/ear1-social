<template>
  <section class="cta">
    <div class="content">
      <div class="txt">
        <h3>Build great relationships with those you admire.</h3>
        <p>With ear1, replies to your DMs are guaranteed!</p>
      </div>
      <div class="btns">
        <StoreButton color="dark" store="appstore" />
        <StoreButton color="dark" store="playstore" />
      </div>
    </div>
  </section>
</template>

<script>
import StoreButton from "@/components/StoreButton.vue";
export default { name: "CallToAction", components: { StoreButton } };
</script>

<style scoped>
.cta {
  padding: 100px 0;
}
.content {
  background-color: var(--primary-400);
  padding: 65px;
  display: flex;
  justify-content: space-between;
  border-radius: 30px;
  align-items: center;
}
.txt {
  display: flex;
  flex-direction: column;
  gap: 30px;
  color: white;
  max-width: 500px;
}
.txt h3 {
  max-width: clamp(314px, 40vw, 450px);
  font-size: clamp(23px, 3vw, 35px);
  font-weight: 700;
  line-height: 115.3%;
  letter-spacing: -0.05em;
}
.txt p {
  font-weight: 500;
  font-size: 18px;
  line-height: 185.6%;
  letter-spacing: -0.03em;
}
.btns {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
}
@media screen and (max-width: 768px) {
  .cta {
    padding: 50px 0 40px;
  }
  .content {
    padding: 60px 20px 35px;
    text-align: center;
    flex-direction: column;
  }
  .txt {
    gap: 20px;
  }
  .btns {
    flex-direction: column-reverse;
    margin-top: 30px;
  }
  .txt h3 {
    width: 100%;
  }
}
</style>
