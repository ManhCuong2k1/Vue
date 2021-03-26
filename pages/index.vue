<template>
  <div>
    <header>
      <div class="top-bar">
        <header class="container mx-auto">
          <div class="">
            <ul class="flex">
              <li class="p-2 text-xs">Đồ chơi</li>
              <li class="p-2 text-xs">Hoa giấy</li>
              <li class="p-2 text-xs">Tái chế</li>
              <li class="p-2 text-xs">Trang trí</li>
            </ul>
          </div>
        </header>
      </div>
      <div class="main-menu">
        <div class="lg:container mx-auto">
          <div class="logo">
            <img
              src="~/assets/img/logo-cachlamhay-final-tiny.png"
              alt=""
              class="w-96 mx-auto p-4"
            />
          </div>
          <div class="menu">
            <ul class="flex justify-center">
              <li class="text-black font-bold px-4 text-sm py-3">TRANG TRÍ</li>
              <li class="text-black font-bold px-4 text-sm py-3">ĐỒ CHƠI</li>
              <li class="text-black font-bold px-4 text-sm py-3">HOA GIẤY</li>
              <li class="text-black font-bold px-4 text-sm py-3">TÁI CHẾ</li>
              <li class="text-black font-bold px-4 text-sm py-3">COVID-19</li>
            </ul>
          </div>
        </div>
      </div>
    </header>
    <main class="container mx-auto">
      <section class="flex block">
        <div class="w-1/3 relative">
          <div class="relative">
            <a href="#">
              <img src="~/assets/img/khay-dung-but-356x220.jpg" alt="" />
            </a>
          </div>
          <div class="w-5/6 absolute text-white top-2/3">
            <h3 class="text-xl"><a href="#">Gợi ý một số cách làm đồ handmade tái chế đơn giản, dễ dàng</a></h3>
            <div class="text-xs">
              <span class="font-bold">Cách làm hay</span> - <span>24/3/2021</span>
            </div>
          </div>
        </div>
        <div class="w-1/3 relative">
          <div class="relative">
            <a href="#">
              <img src="~/assets/img/dreamcatcher-356x220.jpg" alt="" />
            </a>
          </div>
          <div class="w-5/6 absolute text-white top-2/3">
            <h3 class="text-xl"><a href="#">Bật mí những món đồ handmade dễ làm, bạn không nên bỏ qua</a></h3>
            <div class="text-xs">
                <span class="font-bold">Cách làm hay</span> - <span>24/3/2021</span>
            </div>
          </div>
        </div>
        <div class="w-1/3 relative">
          <div class="relative">
            <a href="#">
              <img src="~/assets/img/lo-hoa-bang-giay-bao-cu-356x220.jpg" alt="" />
            </a>
          </div>
          <div class="w-5/6 absolute text-white top-2/3">
            <h3 class="text-xl"><a href="#">Hướng dẫn cách làm một số món đồ handmade tái chế từ giấy</a></h3>
            <div class="text-xs">
                <span class="font-bold">Cách làm hay</span> - <span>24/3/2021</span>
            </div>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<script>
export default {}
</script>

<style>
.top-bar {
  border-bottom: 1px solid rgb(226, 224, 224);
}
.main-menu {
  box-shadow: 0px 25px 20px -32px grey;
}
.container{
  max-width: 1204px !important;
}
.block img{
  filter: brightness(0.7);
}
</style>
