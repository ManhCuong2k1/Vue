<template>
  <div>
    <header>
      <div class="top-bar">
        <header class="container mx-auto">
          <div class="">
            <ul class="flex">
              <li class="p-2 text-xs"><a href="#">Đồ chơi</a></li>
              <li class="p-2 text-xs"><a href="#">Hoa giấy</a></li>
              <li class="p-2 text-xs"><a href="#">Tái chế</a></li>
              <li class="p-2 text-xs"><a href="#">Trang trí</a></li>
            </ul>
          </div>
        </header>
      </div>
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
            <ul class="flex justify-center w-11/12 sm:pl-20 pl-24">
              <li class="text-black font-bold px-4 text-sm py-3"><a href="#">TRANG TRÍ</a></li>
              <li class="text-black font-bold px-4 text-sm py-3"><a href="#">ĐỒ CHƠI</a></li>
              <li class="text-black font-bold px-4 text-sm py-3"><a href="#">HOA GIẤY</a></li>
              <li class="text-black font-bold px-4 text-sm py-3"><a href="#">TÁI CHẾ</a></li>
              <li class="text-black font-bold px-4 text-sm py-3"><a href="#">COVID-19</a></li>
            </ul>
            <div class="search w-1/12 text-center">
              <a href="#"><i class="fas fa-search"></i></a>
            </div>
          </div>
        </div>
      </div>
    </header>
    <main class="container mx-auto">
      <section class="flex flex-wrap block">
        <div class="w-full sm:w-full md:w-1/3 lg:w-1/3 relative" v-for="block in blocks" :key="block.img">
          <div class="relative">
            <a href="#">
              <img :src="`/img/${ block.img }`" :alt="`${ block.img }`" />
            </a>
          </div>
          <div class=" absolute text-white title-block">
            <h3 class="text-xl">{{ block.title }}<a href="#"></a></h3>
            <div class="text-xs">
              <span class="font-bold">Cách làm hay</span> - <span>24/3/2021</span>
            </div>
          </div>
        </div>
      </section>
      <section class="flex flex-wrap main-content mt-4">
        <div class="list-post w-full sm:w-full md:w-8/12 lg:w-8/12">
          <div class="title-content">
            <h3 class="text-xl font-bold">Mới nhất</h3>
            <div class="item-post flex" v-for="post in posts" :key="post.category">
              <div class="img w-4/12">
                <img :src="`/img/${post.img}`" alt="">
              </div>
              <div class="title-post w-8/12">
                <h3><a href="#">{{post.title}}</a></h3>
                <p class="category-date"><span>{{post.category}}</span> CÁCH LÀM HAY - {{ post.date }}</p>
                <div class="description">
                  <p>{{ post.description }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="side-bar w-full sm:w-full md:w-4/12 lg:w-4/12">
          <h3 class="text-xl font-bold">Theo dõi chúng tôi</h3>
          <div class="follow flex">
            <div class="social">
              <i class="fab fa-facebook-f"></i>
              <p>12,050</p>
              <span>Thành viên</span>
            </div>
            <div class="social">
              <i class="fas fa-caret-right"></i>
              <p>2,362</p>
              <span>Người theo dõi</span>
            </div>
          </div>
          <h3 class="text-xl font-bold common">Phổ biến</h3>
          <div class="sidebar-post">
            <div class="flex" v-for="sidebar in sidebars" :key="sidebar.img">
              <div class="img-sidebar w-4/12">
                <img :src="`/img/${ sidebar.img }`" alt="">
              </div>
              <div class="content-sidebar w-8/12">
                <h3>{{ sidebar.title }}</h3>
                <p>{{ sidebar.date }}</p>
              </div>
            </div>
          </div>
          <div class="block_inner">
            <div class="block relative" v-for="blockSidebar in blockSidebars" :key="blockSidebar.img">
              <img class="relative" :src="`/img/${ blockSidebar.img }`" alt="">
              <h3 class="absolute font-bold"><a href="#">{{ blockSidebar.title }}</a></h3>
            </div>
          </div>
        </div>
      </section>
      <section class="covid-country">
        <div class="title">
          <h3 class="text-xl font-bold">COVID-19</h3>
        </div>
        <div class="flex flex-wrap">
          <div class="country w-full sm:w-full md:w-1/5 lg:w-1/5" v-for="covid in covids" :key="covid.number">
            <h3>{{ covid.country }}</h3>
            <p>{{ covid.number }}</p>
            <span>{{ covid.text }}</span>
          </div>
        </div>
      </section>
    </main>
    <footer>
      <div class="footer-main">
        <div class="container mx-auto">
          <div class="logo">
            <img :src="`/img/logo-cachlamhay-final-tiny.png`" alt="">
          </div>
          <div class="about">
            <p>Đến với cửa hàng đồ handmade của chúng tôi thì chắc chắn bạn sẽ cảm nhận được sự khác biệt trong từng sản phẩm. Từ những món quà rất nhỏ như chiếc ví, tấm thiệp… đều có thể biến tấu thành món đồ handmade rất xinh xắn, dễ thương. Tất cả đều được yêu thích và ưa chuộng bởi sự sáng tạo và mang ý nghĩa thật đặc biệt. Dường như, mỗi món quà đều chứa đựng, gửi gắm tâm huyết, tình cảm của người làm…</p>
          </div>
          <div class="contact">
            <p>Contact us:<a href="#">info@pegi.vn</a></p>
          </div>
          <div class="social flex">
            <a href="#"><i class="fab fa-facebook-f"></i></a>
            <a href="#"><i class="fab fa-instagram"></i></a>
            <a href="#"><i class="fab fa-youtube"></i></a>
          </div>
        </div>
      </div>
      <div class="footer-bottom">
        <div class="container mx-auto flex">
          <div class="bottom-left">
            <p>© Copyright 2020 cachlamhay. All Rights Reserved</p>
          </div>
          <div class="bottom-right">
            <ul class="flex">
              <li><a href="#">Đồ chơi</a></li>
              <li><a href="#">Hoa giấy</a></li>
              <li><a href="#">Tái chế</a></li>
              <li><a href="#">Trang trí</a></li>
            </ul>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  data () {
    return {
      blocks: [
        {
          title: 'Gợi ý một số cách làm đồ handmade tái chế đơn giản, dễ dàng',
          img: 'khay-dung-but-356x220.jpg'
        },
        {
          title: 'Bật mí những món đồ handmade dễ làm, bạn không nên bỏ qua',
          img: 'dreamcatcher-356x220.jpg'
        },
        {
          title: 'Hướng dẫn cách làm một số món đồ handmade tái chế từ giấy',
          img: 'lo-hoa-bang-giay-bao-cu-356x220.jpg'
        }
      ],
      covids: [
        {
          country: 'Việt Nam',
          number: '2,576',
          text: 'Ca xác nhận'
        },
        {
          country: 'Việt Nam',
          number: '2,265',
          text: 'Ca hồi phục'
        },
        {
          country: 'Việt Nam',
          number: '276',
          text: 'Ca đang điều trị'
        },
        {
          country: 'Việt Nam',
          number: '35',
          text: 'Tử vong'
        },
        {
          country: 'Thế giới',
          number: '125,087,561',
          text: 'Ca xác nhận dương tính'
        }
      ],
      sidebars: [
        {
          img: 'khay-dung-but-356x220.jpg',
          title: 'Gợi ý một số cách làm đồ handmade tái chế đơn...',
          date: '14/03/2021'
        },
        {
          img: 'dreamcatcher-356x220.jpg',
          title: 'Bật mí những món đồ handmade dễ làm, bạn không nên...',
          date: '14/03/2021'
        },
        {
          img: 'lo-hoa-bang-giay-bao-cu-356x220.jpg',
          title: 'Hướng dẫn cách làm một số món đồ handmade tái chế ...',
          date: '14/03/2021'
        },
        {
          img: 'may-bay-truc-thang-bang-nhua-696x392.jpg',
          title: 'Gợi ý cách làm một số món đồ chơi từ chai...',
          date: '14/03/2021'
        },
        {
          img: 'thiep-handmade-696x392.jpg',
          title: 'Bật mí 5 món quà handmade 8/3 ngọt ngào, ý nghĩa',
          date: '14/03/2021'
        }
      ],
      posts: [
        {
          img: 'may-bay-truc-thang-bang-nhua-696x392.jpg',
          title: 'Gợi ý cách làm một số món đồ chơi từ chai nhựa cho bé',
          category: 'ĐỒ CHƠI',
          date: '14/03/2021',
          description: 'Nếu biết tận dụng và tái chế chai nhựa thì bạn sẽ không chỉ mang đến cho bé yêu nhà bạn những món đồ chơi độc lạ, thú vị. Mà...'
        },
        {
          img: 'thiep-handmade-696x392.jpg',
          title: 'Bật mí 5 món quà handmade 8/3 ngọt ngào, ý nghĩa',
          category: 'QUÀ TẶNG',
          date: '12/03/2021',
          description: 'Mùng 8 tháng 3, chắc chắn nhiều phái nam đang vô cùng băn khoăn và trăn trở. Khi không biết nên tặng quà gì cho đối phương. Nếu bạn cũng...'
        },
        {
          img: 'thiep-giay-xoan-696x556.png',
          title: 'Cách làm một số món quà handmade 8/3 đơn giản, ý nghĩa',
          category: 'QUÀ TẶNG',
          date: '10/03/2021',
          description: 'Bạn được trời phú cho một chút “hoa tay” và sở hữu sự khéo léo cùng tính kiên nhẫn, tỉ mỉ? Vào dịp 8/3 này, bạn muốn dành sự bất...'
        },
        {
          img: '8.3-696x464.jpg',
          title: '8/3 là ngày gì? Nguồn gốc và ý nghĩa của ngày 8/3',
          category: 'QUÀ TẶNG',
          date: '08/03/2021',
          description: 'Vào ngày 8/3 hằng năm, hầu như ai cũng thấy phái nữ sẽ được tặng hoa, tặng quà và được nhận những lời chúc ý nghĩa ngọt ngào. Vậy 8/3...'
        },
        {
          img: 'tohe-shop.jpg',
          title: 'Mua quà 8/3 ở đâu? Top 4 địa chỉ nổi tiếng ở Hà Nội',
          category: 'QUÀ TẶNG',
          date: '05/03/2021',
          description: '8/3 đã cận kề. Thế nhưng, các phái nam lại đang rất băn khoăn khi không biết mua quà 8/3 ở đâu? Để tặng cho những người phụ nữ mà...'
        },
        {
          img: 'thiep-handmade-696x392.jpg',
          title: 'Điểm danh những món quà handmade 8/3 ý nghĩa',
          category: 'QUÀ TẶNG',
          date: '04/03/2021',
          description: 'Dường như ai cũng biết, 8/3 là ngày mà phái mạnh sẽ có cơ hội thể hiện tình cảm cũng như sự quý mến đối với những người phụ nữ...'
        },
        {
          img: 'Dừa’s-Craft-696x696.jpg',
          title: 'Top 4 shop mua nguyên liệu handmade tốt nhất ở Hà Nội',
          category: 'TÁI CHẾ',
          date: '18/02/2021',
          description: 'Chắc hẳn, các bạn đã từng đau đầu. Vì không biết nên chọn mua quà gì cho bạn bè, người thân vào những dịp đặc biệt. Gợi ý, bạn có...'
        },
        {
          img: 'gau-bong.jpg',
          title: 'Top 5 món quà tặng bạn gái cực kỳ ý nghĩa không nên bỏ qua',
          category: 'QUÀ TẶNG',
          date: '14/03/2021',
          description: 'Một trong những cách để các bạn nam dễ dàng thể hiện được tình cảm chân thành của mình đến nửa kia, đó chính là tặng quà vào những ngày...'
        }
      ],
      blockSidebars: [
        {
          img: 'tu-lam-do-choi-bang-chu-cai-cho-be-tu-nap-chai-nhua-696x392.png',
          title: 'Tự làm đồ chơi bảng chữ cái cho bé từ nắp chai nhựa'
        },
        {
          img: 'bup-be-len.jpg',
          title: 'Hướng dẫn cách làm 3 món đồ handmade bằng len đơn giản'
        },
        {
          img: 'cach-tu-lam-do-choi-domino-cho-be-4k-696x392.png',
          title: 'Cách tự làm đồ chơi Domino cho bé'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
  @import '~/assets/sass/main.scss';
</style>
