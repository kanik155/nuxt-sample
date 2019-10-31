<template>
  <div class="header">
    <nav class="navbar has-shadow" role="navigation" aria-label="main navigation">
      <div class="navbar-brand">
        <a class="navbar-item" href="https://bulma.io">
          <img src="https://bulma.io/images/bulma-logo.png" width="112" height="28" />
        </a>

        <a
          role="button"
          class="navbar-burger burger"
          :class="{ 'is-active': isActive }"
          aria-label="menu"
          aria-expanded="false"
          @click="toggleMenu"
        >
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
          <span aria-hidden="true"></span>
        </a>
      </div>

      <div class="navbar-menu" :class="{'is-active': isActive}">
        <div class="navbar-start">
          <nuxt-link class="navbar-item" to="/">Home</nuxt-link>
          <nuxt-link class="navbar-item" to="/settings">Settings</nuxt-link>

          <div class="navbar-item has-dropdown is-hoverable">
            <a class="navbar-link">About</a>

            <div class="navbar-dropdown">
              <nuxt-link class="navbar-item" to="/license">ライセンス情報</nuxt-link>
              <hr class="navbar-divider" />
              <nuxt-link class="navbar-item" to="/contact">お問い合わせ</nuxt-link>
            </div>
          </div>
        </div>

        <div class="navbar-end">
          <div class="navbar-item">
            <div class="buttons">
              <a class="button is-primary">Log in</a>
            </div>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<style>
.menu {
  list-style: none;
  padding: 0;
  background-color: #eee;
}
.menu li {
  display: inline-block;
  padding: 5px;
}
</style>

<script>
export default {
  data() {
    return {
      isActive: false
    };
  },
  methods: {
    toggleMenu(e) {
      this.isActive = !this.isActive;
    }
  }
};
</script>