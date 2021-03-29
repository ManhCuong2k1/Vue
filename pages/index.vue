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
                <div class="description">
                  <p>{{ post.description }}</p>
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
          img: '~/assets/img/may-bay-truc-thang-bang-nhua-696x392.jpg',
          title: 'Gợi ý cách làm một số món đồ chơi từ chai nhựa cho bé',
          category: 'Đồ chơi',
          date: '14/03/2021',
          description: 'Nếu biết tận dụng và tái chế chai nhựa thì bạn sẽ không chỉ mang đến cho bé yêu nhà bạn những món đồ chơi độc lạ, thú vị. Mà...'
        },
        {
          img: '/_nuxt/assets/img/a.png',
          title: 'Bật mí 5 món quà handmade 8/3 ngọt ngào, ý nghĩa',
          category: 'QUÀ TẶNG',
          date: '12/03/2021',
          description: 'Mùng 8 tháng 3, chắc chắn nhiều phái nam đang vô cùng băn khoăn và trăn trở. Khi không biết nên tặng quà gì cho đối phương. Nếu bạn cũng...'
        },
        {
          img: '/_nuxt/assets/img/thiep-giay-xoan-696x556.png',
          title: 'Cách làm một số món quà handmade 8/3 đơn giản, ý nghĩa',
          category: 'QUÀ TẶNG',
          date: '10/03/2021',
          description: 'Bạn được trời phú cho một chút “hoa tay” và sở hữu sự khéo léo cùng tính kiên nhẫn, tỉ mỉ? Vào dịp 8/3 này, bạn muốn dành sự bất...'
        },
        {
          img: '/_nuxt/assets/img/8.3-696x464.jpg',
          title: '8/3 là ngày gì? Nguồn gốc và ý nghĩa của ngày 8/3',
          category: 'QUÀ TẶNG',
          date: '08/03/2021',
          description: 'Vào ngày 8/3 hằng năm, hầu như ai cũng thấy phái nữ sẽ được tặng hoa, tặng quà và được nhận những lời chúc ý nghĩa ngọt ngào. Vậy 8/3...'
        },
        {
          img: '/_nuxt/assets/img/tohe-shop.jpg',
          title: 'Mua quà 8/3 ở đâu? Top 4 địa chỉ nổi tiếng ở Hà Nội',
          category: 'QUÀ TẶNG',
          date: '05/03/2021',
          description: '8/3 đã cận kề. Thế nhưng, các phái nam lại đang rất băn khoăn khi không biết mua quà 8/3 ở đâu? Để tặng cho những người phụ nữ mà...'
        },
        {
          img: '/_nuxt/assets/img/thiep-handmade-696x392.jpg',
          title: 'Điểm danh những món quà handmade 8/3 ý nghĩa',
          category: 'QUÀ TẶNG',
          date: '04/03/2021',
          description: 'Dường như ai cũng biết, 8/3 là ngày mà phái mạnh sẽ có cơ hội thể hiện tình cảm cũng như sự quý mến đối với những người phụ nữ...'
        },
        {
          img: '/_nuxt/assets/img/Dừa’s-Craft-696x696.jpg',
          title: 'Top 4 shop mua nguyên liệu handmade tốt nhất ở Hà Nội',
          category: 'TÁI CHẾ',
          date: '18/02/2021',
          description: 'Chắc hẳn, các bạn đã từng đau đầu. Vì không biết nên chọn mua quà gì cho bạn bè, người thân vào những dịp đặc biệt. Gợi ý, bạn có...'
        },
        {
          img: '/_nuxt/assets/img/gau-bong.jpg',
          title: 'Top 5 món quà tặng bạn gái cực kỳ ý nghĩa không nên bỏ qua',
          category: 'QUÀ TẶNG',
          date: '14/03/2021',
          description: 'Một trong những cách để các bạn nam dễ dàng thể hiện được tình cảm chân thành của mình đến nửa kia, đó chính là tặng quà vào những ngày...'
        }
      ]
    }
  }
}
</script>

<style>

</style>
