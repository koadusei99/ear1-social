<template>
  <section class="footer">
    <div class="brand">
      <img class="logo" src="../assets/logo-foot.svg" alt="" />
      <p class="copyright">
        <span><img src="../assets/copy.svg" alt="" /></span> 2020 ear1Social
      </p>
      <p class="policy">Privacy policy | Terms of service</p>
    </div>
    <div class="navs">
      <div class="company">
        <h4>Company</h4>
        <ul class="list">
          <li>About Us</li>
          <li>FAQs</li>
          <li>Contact Us</li>
        </ul>
      </div>
      <div class="touch">
        <h4>Get In Touch</h4>
        <p>Questions or feedback?, we would love to hear from you.</p>
        <ul class="socials list">
          <li><img src="../assets/fb.svg" alt="" /></li>
          <li><img src="../assets/twitter.svg" alt="" /></li>
          <li><img src="../assets/ig.svg" alt="" /></li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
export default { name: "Footer" };
</script>

<style scoped>
.footer {
  display: flex;
  justify-content: space-between;
  padding: 90px 100px;
  background-color: var(--grey-600);
}
.brand {
  display: flex;
  flex-direction: column;
  gap: 16px;
}
.navs {
  display: flex;
  gap: 200px;
}
.logo {
  margin-bottom: 10px;
  width: 60px;
}
.copyright {
  color: var(--grey-100);
  font-weight: 500;
  font-size: clamp(18px, 2vw, 20px);
  line-height: 84.6%;
  letter-spacing: -0.03em;
  display: flex;
  gap: 7px;
  align-items: center;
}
.policy {
  color: var(--grey-300);
  font-size: (14px, 2vw, 16px);
  line-height: 84.6%;
  letter-spacing: -0.03em;
}
.company {
  display: flex;
  flex-direction: column;
  gap: 30px;
}
.company .list {
  display: flex;
  flex-direction: column;
  gap: 25px;
}
.touch {
  max-width: 220px;
  display: flex;
  flex-direction: column;
  gap: 30px;
}
.touch p {
  font-size: clamp(16px, 2vw, 18px);
  line-height: 132.6%;
  letter-spacing: -0.03em;
}
.socials {
  display: flex;
  gap: 25px;
  margin-top: -10px;
  align-items: center;
}
h4 {
  color: var(--grey-100);
  font-size: clamp(18px, 2vw, 20px);
  line-height: 84.6%;
  font-weight: 500;
  letter-spacing: -0.03em;
}
.company,
.touch {
  color: var(--grey-300);
}
@media screen and (max-width: 768px) {
  .footer {
    flex-direction: column;
    justify-content: flex-start;
    padding: 50px 25px;
  }
  .navs {
    margin-top: 50px;
    flex-direction: column;
    gap: 50px;
  }
  .touch {
    max-width: 100%;
  }
}
</style>
