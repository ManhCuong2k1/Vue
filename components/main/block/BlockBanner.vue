<template>
    <section class="flex flex-wrap block">
      <block-item
        v-for="block in blocks"
        :key="block.img"
        :img="block.img"
        :title="block.title"></block-item>
    </section>
</template>

<script>
import BlockItem from './BlockItem'

export default {
  components: {
    BlockItem
  },
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
      ]
    }
  }
}
</script>
