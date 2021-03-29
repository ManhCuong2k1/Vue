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
          <div class="w-5/6 absolute text-white title-block">
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
          <div class="w-5/6 absolute text-white title-block">
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
          <div class="w-5/6 absolute text-white title-block">
            <h3 class="text-xl"><a href="#">Hướng dẫn cách làm một số món đồ handmade tái chế từ giấy</a></h3>
            <div class="text-xs">
                <span class="font-bold">Cách làm hay</span> - <span>24/3/2021</span>
            </div>
          </div>
        </div>
      </section>
      <section class="flex main-content mt-4">
        <div class="list-post w-9/12">
          <div class="title-content">
            <h3 class="text-xl font-bold">Mới nhất</h3>
            <div class="item-post flex" v-for="post in posts" :key="post.category">
              <div class="img w-3/12">
                <img :src="post.img" alt="">
              </div>
              <div class="title-post w-9/12">
                <h3><a href="#">{{post.title}}</a></h3>
                <p><span>{{post.category}}</span> CÁCH LÀM HAY - {{ post.date }}</p>
                <div class="desciption">
                  <p>{{ post.desciption }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="side-bar w-3/12">
          <h3>Theo dõi chúng tôi</h3></div>
      </section>
    </main>
  </div>
</template>

<script>
export default {
  data () {
    return {
      posts: [
        {
          img: '_nuxt/assets/img/may-bay-truc-thang-bang-nhua-696x392.jpg',
          title: 'Gợi ý cách làm một số món đồ chơi từ chai nhựa cho bé',
          category: 'Đồ chơi',
          date: '14/03/2021',
          description: 'Nếu biết tận dụng và tái chế chai nhựa thì bạn sẽ không chỉ mang đến cho bé yêu nhà bạn những món đồ chơi độc lạ, thú vị. Mà...'
        }
      ]
    }
  }
}
</script>

<style>

</style>
