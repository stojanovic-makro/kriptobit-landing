<template>
  <div class="main-page-wrapper" style="min-width: 810px">
    <header>
      <div class="logo">
        <img style="margin-right: 3px" src="/icons/kriptobit-left.svg" alt="logo">
        <img style="margin-right: 5px" src="/icons/kriptobit-right.svg" alt="logo">
        <img src="/icons/kriptobit-text.svg" alt="logo">
      </div>
      <img src="/icons/burger.svg" alt="menu">
    </header>
    <main>
      <section class="row" style="justify-content: space-between; flex-wrap: wrap">
        <div style="max-width: 744px">
          <p style="font-family: 'Atyp Display Medium'; font-size: 64px; line-height: 92px;"><span>Najsigurnija</span> kripto menjacnica za razmenu digitalne imovine !</p>
          <p class="t1">Verujemo u svet ekonomije deljenja i decentralizacije, pa smo zamislili i stvorili alate i platforme nove generacije za rudare i trgovce kriptovalutama.</p>
          <div class="row" style="margin-top: 64px">
            <input class="email-input" type="email" placeholder="Vaš Email....">
            <Button label="PRIJAVI SE" />
          </div>
        </div>
        <div>
          <img style="height: 480px; width: 480px" src="/icons/union.svg" alt="union">
        </div>
      </section>
    </main>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
// eslint-disable-next-line
import Button from '~/components/ui/Button.vue'

export default Vue.extend({
  name: 'IndexPage',
  components: { Button }
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
  display: flex;
  padding-left: 96px;
  padding-right: 96px;
}

.main-page-wrapper {
  border-left: 1px solid $grey;
  border-right: 1px solid $grey;
  height: 100vh;
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