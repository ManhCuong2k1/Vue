<template>
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
          <post-sidebar
            v-for="post in sidebars"
            :key="post.img"
            :img="post.img"
            :title="post.title"
            :date="post.date"></post-sidebar>
        </div>
        <div class="block_inner">
          <blockitem-bar
            v-for="block in blockSidebars"
            :key="block.img"
            :img="block.img"
            :title="block.title"></blockitem-bar>
        </div>
    </div>
</template>

<script>
import BlockitemBar from './BlockitemBar.vue'
import PostSidebar from './PostSidebar.vue'
export default {
  components: {
    BlockitemBar,
    PostSidebar
  },
  data () {
    return {
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
