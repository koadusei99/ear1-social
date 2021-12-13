<template>
  <header>
    <nav>
      <div class="brand">
        <router-link to="/"
          ><img src="../assets/logo-green.svg" alt="Logo Green"
        /></router-link>
        <button @click="toggleNav" id="nav-toggle">
          <img
            :src="require(`../assets/${toggleIcon}.svg`)"
            width="40"
            alt=""
          />
        </button>
      </div>
      <ul :class="`${expanded ? 'show' : ''} navlinks list`">
        <li><router-link class="link" to="/">About</router-link></li>
        <li><router-link class="link" to="/">FAQs</router-link></li>
        <li>
          <router-link class="link" to="/">Contact Us</router-link>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return { color: "red", expanded: false };
  },
  methods: {
    toggleNav() {
      this.expanded = !this.expanded;
    },
  },
  computed: {
    toggleIcon() {
      return this.expanded ? "minus" : "hamburger";
    },
  },
};
</script>

<style>
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 50px 100px;
}
.brand {
  display: flex;
  justify-content: space-between;
}
#nav-toggle {
  display: none;
}

.navlinks {
  display: flex;
  gap: 40px;
}
.navlinks .link {
  color: var(--grey-500);
  font-size: 16px;
  font-weight: 500;
  background-color: v-bind(color);
}
.link:hover {
  color: var(--primary-400);
  text-decoration: underline;
}
@media screen and (max-width: 768px) {
  nav {
    padding: 50px 20px;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;
    gap: 40px;
    position: relative;
  }
  .brand {
    width: 100%;
  }
  #nav-toggle {
    display: flex;
    background-color: transparent;
    border: none;
    cursor: pointer;
  }
  .navlinks {
    padding: 10px 30px 30px;
    position: absolute;
    flex-direction: column;
    top: 150px;
    left: 0;
    gap: 30px;
    width: 100%;
    opacity: 0;
    /* transform: translateY(-1000%); */
    transition: all 200ms ease-in;
    background: #ffffff;
    z-index: 10;
    box-shadow: 0 2px 0 1px rgba(0, 0, 0, 0.2);
  }
  .navlinks.show {
    opacity: 1;
    /* transform: translateY(0%); */
  }
  .navlinks .link {
    font-size: 18px;
    font-weight: 600;
  }
}
</style>
