<template>
    <div class="main-menu">
        <div class="container mx-auto">
            <div class="logo">
                <img
                src="/img/logo-cachlamhay-final-tiny.png"
                alt=""
                class="w-96 mx-auto p-4"
                />
            </div>
            <div class="menu flex flex-wrap">
                <div class="md:hidden icon-menu" id="icon-menu" @click="toggleMenu">
                    <i class="fas fa-bars"></i>
                </div>
                <ul class="md:flex justify-center w-11/12 sm:pl-20 pl-24 nav uppercase" id="nav">
                    <li class="text-black font-bold px-4 text-sm py-3"><a href="#">Trang trí</a></li>
                    <li class="text-black font-bold px-4 text-sm py-3"><a href="#">Đồ chơi</a></li>
                    <li class="text-black font-bold px-4 text-sm py-3"><a href="#">Hoa giấy</a></li>
                    <li class="text-black font-bold px-4 text-sm py-3"><a href="#">Tái chế</a></li>
                    <li class="text-black font-bold px-4 text-sm py-3"><a href="#">Covid-19</a></li>
                </ul>
                <div class="search w-1/12 text-center search" id="search">
                <a href="#"><i class="fas fa-search"></i></a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  methods: {
    toggleMenu () {
      document.getElementById('nav').classList.toggle('toogle-nav')
      document.getElementById('icon-menu').classList.toggle('toggle-icon-menu')
    }
  }
}
</script>
