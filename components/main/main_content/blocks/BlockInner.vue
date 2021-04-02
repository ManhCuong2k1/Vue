<template>
    <div class="list-post w-full sm:w-full md:w-8/12 lg:w-8/12">
          <div class="title-content">
            <h3 class="text-xl font-bold">Mới nhất</h3>
            <inner-item
              v-for="post in posts"
              :key="post.img"
              :title="post.title"
              :category="post.category"
              :img="post.img"
              :date="post.date"
              :description="post.description"></inner-item>
          </div>
        </div>
</template>

<script>
import InnerItem from './InnerItem.vue'
export default {
  components: {
    InnerItem
  },
  data () {
    return {
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
      ]
    }
  }
}
</script>
