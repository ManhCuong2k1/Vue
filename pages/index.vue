<template>
  <div>
    <header>
      <top-bar></top-bar>
      <main-menu></main-menu>
    </header>
    <main class="container mx-auto">
      <block-banner></block-banner>
      <section class="flex flex-wrap main-content mt-4">
        <block-inner></block-inner>
        <side-bar></side-bar>
      </section>
      <covid-country></covid-country>
    </main>
    <footer>
      <footer-main></footer-main>
      <footer-bottom></footer-bottom>
    </footer>
  </div>
</template>

<script>
import TopBar from '../components/header/TopBar.vue'
import MainMenu from '../components/header/MainMenu.vue'
import BlockBanner from '../components/main/block/BlockBanner.vue'
import BlockInner from '../components/main/main_content/blocks/BlockInner.vue'
import SideBar from '../components/main/main_content/sidebar/Sidebar.vue'
import CovidCountry from '../components/main/covid/CovidCountry.vue'
import FooterMain from '../components/footer/FooterMain.vue'
import FooterBottom from '../components/footer/FooterBottom.vue'

export default {
  components: {
    TopBar,
    MainMenu,
    BlockBanner,
    BlockInner,
    SideBar,
    CovidCountry,
    FooterMain,
    FooterBottom
  }
}
</script>

<style lang="scss">
  @import '~/assets/sass/main.scss';
</style>
