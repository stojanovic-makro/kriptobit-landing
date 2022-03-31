<template>
  <div class="main-page-wrapper">
    <header>
      <transition name="home">
        <HeaderMenu v-show="isMenu" style="position: absolute; top: 72px; left: 96px" />
      </transition>
      <div class="logo">
        <img style="margin-right: 3px" src="~/static/icons/kriptobitLeft.svg" alt="logo">
        <img style="margin-right: 5px" src="~/static/icons/kriptobitRight.svg" alt="logo">
        <img src="~/static/icons/kriptobitText.svg" alt="logo">
      </div>
      <img v-if="isMenu" src="~/static/icons/close.svg" style="cursor: pointer" alt="menu" @click="isMenu = !isMenu">
      <img v-else src="~/static/icons/burger.svg" style="cursor: pointer" alt="menu" @click="isMenu = !isMenu">
    </header>
    <main>
      <section style="padding-top: 145px; padding-bottom: 128px">
        <div>
          <p style="font-family: 'Atyp Display Medium'; font-size: 64px; line-height: 92px; margin-top: 0">Blog</p>
          <p style="max-width: 744px" class="t1">This is a blog page.</p>
        </div>
      </section>
    </main>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
// eslint-disable-next-line
import Button from '~/components/ui/Button.vue'
import HeaderMenu from '~/components/ui/headerMenu.vue'

export default Vue.extend({
  name: 'Blog',
  head: {
    title: 'KRIPTOBIT | Blog'
  },
  components: { Button, HeaderMenu },
  data: () => ({
    isMenu: false
  })
})
</script>

<style lang="scss">
header {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  height: 72px;
  border-bottom: 1px solid $grey;
  padding-left: 96px;
  padding-right: 96px;
}

section {
  border-bottom: 1px solid $grey;
  display: flex;
  padding-left: 96px;
  padding-right: 96px;
}

.main-page-wrapper {
  border-left: 1px solid $grey;
  border-right: 1px solid $grey;
}

.logo {
  width: fit-content;
  height: fit-content;
  display: flex;
  flex-direction: row;
  flex-wrap: nowrap;
  justify-content: center;
  align-items: center;
}

.email-input {
  font-family: 'Atyp Display Regular';
  font-size: 16px;
  background: none;
  color: $grey;
  width: 361px;
  height: 48px;
  border: 1px solid white;
  padding-left: 24px;
  padding-right: 24px;
}
</style>