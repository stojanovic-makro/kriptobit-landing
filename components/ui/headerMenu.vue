<template>
  <div class="menu">
    <div style="display: flex; flex-direction: row; flex-wrap: wrap; margin-bottom: 40px">
      <div style="align-items: start; flex-grow: 1">
        <img style="width: 480px; height: 251px" src="~/static/icons/logoMenu.svg" alt="logo">
      </div>
      <div class="menu__items">
        <NuxtLink v-for="route in routes" :key="route.path" :class="{ active: route.path === $route.path }" :to="route.path">{{ route.title }}</NuxtLink>
      </div>
      <div class="menu__items-right">
        <p>Privacy policy</p>
        <p>Cookies</p>
        <p>Terms of use</p>
      </div>
    </div>

    <div class="row" style="justify-content: space-between; align-items: end">
      <div style="width: 213px" class="menu__grey-text">
        Najsigurnija kripto menjacnica za razmenu digitalne imovine !
      </div>
      <div class="menu__grey-text">
        &copy; 2022
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderMenu',
  data: () => ({
    routes: [
      { path: '/', title: 'Home',  },
      { path: '/blog', title: 'Blog' },
      { path: '/dashboard', title: 'Dashboard' },
      { path: '/about', title: 'About Us' },
    ]
  })
}
</script>

<style lang="scss">
.active {
  color: $brand !important;
}

.menu {
  padding-top: 48px;
  padding-bottom: 48px;
  padding-left: 96px;
  padding-right: 96px;
  border: 1px solid $grey;
  backdrop-filter: blur(1.5rem);
  width: calc(100% - 386px);
  background-color: rgba(0, 0, 0, 0.35);
  &__items {
    padding-left: 40px;
    margin-top: 40px;
    display: flex;
    flex-direction: column;
    flex-grow: 1;
    font-family: 'Atyp Display Thin';
    font-size: 72px;
    line-height: 101px;
    gap: 16px;
    a {
      text-decoration: none;
      color: white;
      transition: 0.3s;
      cursor: pointer;
      margin: 0;
      &:hover {
        color: $brand
      }
    }
  }
  &__items-right {
    flex-grow: 1;
    display: flex;
    flex-direction: column;
    justify-content: end;
    align-items: end;
    padding-bottom: 100px;
    font-family: 'Atyp Display Semibold';
    p {
      transition: 0.3s;
      cursor: pointer;
      margin: 10px;
      font-size: 16px;
      line-height: 23px;
      &:hover {
        color: $brand
      }
    }
  }
  &__grey-text {
    font-family: 'Atyp Display Regular';
    font-size: 16px;
    line-height: 23px;
    color: $grey
  }
}
</style>