<template>
  <div>
    <nav class="nav-bar">
      <div class="header">

        <button class="header_menu " @click="showMenu()">
          <i class="fa fa-bars"></i>
        </button>

        <a href="#">
          <img src="@/assets/images/logo.jpg" alt="pileton logo" class="header_logo md">
        </a>

        <Categories />

        <Search />

      </div>
     </nav>

    <FooterMenu />

    <Menu v-if="isMenu" @closeMenu="showMenu()"/>

  </div>
</template>

<script>
import Menu from '@/components/header/menu'
import FooterMenu from '@/components/header/footerMenu'
import Categories from '@/components/header/categories'
import Search from '@/components/header/search'

export default {
  data() {
    return {
      isMenu: false
    }
  },
  components: {
    Categories,
    Search,
    Menu,
    FooterMenu
  },
  methods: {
    showMenu() {
      this.isMenu = !this.isMenu

    }
  }
}
</script>
