<template>
  <div id="app">
    <Navbar></Navbar>
    <Hero />
    <div class="home-main">
      <section class="features">
        <Feature :feature="features[0]" />
        <Feature :feature="features[1]" />
        <Feature :feature="features[2]" center />
      </section>
      <CallToAction />
    </div>
    <Footer />
  </div>
</template>
<script>
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import Feature from "@/components/Feature.vue";
import CallToAction from "@/components/CallToAction.vue";
import Footer from "@/components/Footer.vue";

export default {
  components: {
    Navbar,
    Hero,
    Feature,
    CallToAction,
    Footer,
  },
  data() {
    return {
      features: [
        {
          title: "Get in touch with those that inspire you.",
          emph: "inspire",
          text: "ear1 provides a more efficient and faster way for you to reach out to those who inspires you, either in your career, or any other field of interest, and build great relationships with them.",
          img: "f1.png",
        },
        {
          title: "You have zero chances of not being replied.",
          emph: "zero",
          text: "Sending a DM should no more be an issue of shooting your shot or trying your luck. You’re paying, so you’re definitely going to get a response, and not just a response, but a conversation.",
          img: "f2.png",
        },
        {
          title:
            "There’s no better way of reaching out to those who inspires you.",
          emph: "better way",
          text: "Ear1 lets influencers charge you a small fee to have a conversation with them. Being required to pay filters out all the unserious people so your favourite influencers can respond to you faster.",
          img: "f3.png",
        },
      ],
    };
  },
};
</script>
<style>
.home-main {
  padding: 0 80px;
}
/* didnt work in component */
.txt .emph {
  color: var(--primary-400);
  font-style: italic;
}
@media screen and (max-width: 768px) {
  .home-main {
    padding: 0 20px;
  }
}
</style>
