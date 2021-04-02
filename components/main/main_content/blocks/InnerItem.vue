<template>
    <div class="item-post flex">
        <div class="img w-4/12">
            <img :src="`/img/${ img }`" alt="">
        </div>
        <div class="title-post w-8/12">
        <h3><a href="#">{{ title }}</a></h3>
        <p class="category-date"><span>{{ category }}</span> CÁCH LÀM HAY - {{ date }}</p>
        <div class="description">
            <p>{{ description }}</p>
        </div>
        </div>
    </div>
</template>

<script>
export default {
  props: ['img', 'title', 'date', 'category', 'description']
}
</script>
