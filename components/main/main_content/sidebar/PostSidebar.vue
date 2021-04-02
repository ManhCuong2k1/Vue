<template>
    <div class="flex">
        <div class="img-sidebar w-4/12">
            <img :src="`/img/${ img }`" alt="">
        </div>
        <div class="content-sidebar w-8/12">
            <h3>{{ title }}</h3>
            <p>{{ date }}</p>
        </div>
    </div>
</template>

<script>
export default {
  props: ['img', 'date', 'title']
}
</script>
