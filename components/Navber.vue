<template>
  <header>
    <nav class="container">
      <div class="branding">
        <NuxtLink class="header" to="/">Fashion Fution</NuxtLink>
      </div>
      <div class="nav-links">
        <ul v-show="!mobile">
          <NuxtLink class="link" to="/">Home</NuxtLink>
          <NuxtLink class="link" to="/about">About</NuxtLink>
          <NuxtLink class="link" to="/products">Products</NuxtLink>
          <NuxtLink class="link" to="/dashboard">Dashboard</NuxtLink>
        </ul>
      </div>
    </nav>
    <div>
      <svg
        aria-hidden="true"
        focusable="false"
        data-prefix="far"
        data-icon="bars"
        class="menu-icon svg-inline--fa fa-bars fa-w-14"
        role="img"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 448 512"
        @click="toggleMobileNav"
        v-show="mobile"
      >
        <path
          fill="currentColor"
          d="M436 124H12c-6.627 0-12-5.373-12-12V80c0-6.627 5.373-12 12-12h424c6.627 0 12 5.373 12 12v32c0 6.627-5.373 12-12 12zm0 160H12c-6.627 0-12-5.373-12-12v-32c0-6.627 5.373-12 12-12h424c6.627 0 12 5.373 12 12v32c0 6.627-5.373 12-12 12zm0 160H12c-6.627 0-12-5.373-12-12v-32c0-6.627 5.373-12 12-12h424c6.627 0 12 5.373 12 12v32c0 6.627-5.373 12-12 12z"
        ></path>
      </svg>
    </div>
    <transition name="mobile-nav">
      <ul class="mobile-nav" v-show="mobileNav">
        <NuxtLink class="link" to="/">Home</NuxtLink>
        <NuxtLink class="link" to="/about">About</NuxtLink>
        <NuxtLink class="link" to="/product">Product</NuxtLink>
        <NuxtLink class="link" to="/dashboard">Dashboard</NuxtLink>
      </ul>
    </transition>
  </header>
</template>

<script>
export default {
  data() {
    return {
      mobile: null,
      mobileNav: null,
      windowWidth: null,
      email: '',
    }
  },
  created() {
    window.addEventListener('resize', this.checkScreen)
    this.checkScreen()
  },
  methods: {
    checkScreen() {
      this.windowWidth = window.innerWidth
      if (this.windowWidth <= 750) {
        this.mobile = true
        return
      }
      this.mobile = false
      this.mobileNav = false
      return
    },
    toggleMobileNav() {
      this.mobileNav = !this.mobileNav
    },
  },
}
</script>

<style scoped>
header {
  background-color: #000;
  padding: 0 25px;
  z-index: 99;
  position: sticky;
  top: 0;
  left: 0;
}

.link {
  font-weight: 500;
  padding: 0 8px;
  transition: 0.3s color ease;
  color: #fff;
  text-decoration: none;
  font-family: 'Rubik', sans-serif;
}

.link:hover {
  color: #1eb8b8;
}

nav {
  display: flex;
  padding: 15px 0;
}

.branding {
  display: flex;
  align-items: center;
}
.header {
  background: #13cfcf;
  background: repeating-radial-gradient(
    circle farthest-corner at center center,
    #13cfcf 0%,
    #cf87a8 100%
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-family: 'Belanosima', sans-serif;
  font-size: 2rem;
}
.nav-links {
  position: relative;
  display: flex;
  flex: 1;
  align-items: center;
  justify-content: flex-end;
}

ul {
  margin-right: 32px;
}

ul .link {
  margin-right: 32px;
}

.link:last-child {
  margin-right: 0;
}

.menu-icon {
  position: absolute;
  cursor: pointer;
  top: 20px;
  right: 25px;
  height: 25px;
  width: auto;
  color: #fff;
}

.mobile-nav {
  padding: 20px;
  width: 70%;
  max-width: 250px;
  display: flex;
  flex-direction: column;
  position: fixed;
  height: 100%;
  background-color: #303030;
  top: 0;
  left: 0;
}

.mobile-nav .link {
  padding: 15px 0;
  color: #fff;
}

.mobile-nav-enter-active,
.mobile-nav-leave-active {
  transition: all 1s ease;
}

.mobile-nav-enter {
  transform: translateX(-250px);
}

.mobile-nav-enter-to {
  transform: translateX(0);
}

.mobile-nav-leave-to {
  transform: translateX(-250px);
}
</style>
