<template>
    <section class="covid-country">
        <div class="title">
          <h3 class="text-xl font-bold">COVID-19</h3>
        </div>
        <div class="flex flex-wrap">
          <country-item
            v-for="covid in covids"
            :key="covid.id"
            :country="covid.country"
            :number="covid.number"
            :text="covid.text"></country-item>
        </div>
      </section>
</template>

<script>
import CountryItem from './CountryItem.vue'
export default {
  components: {
    CountryItem
  },
  data () {
    return {
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
      ]
    }
  }
}
</script>
