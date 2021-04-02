<template>
     <div class="block relative">
        <img class="relative" :src="`/img/${ img }`" alt="">
        <h3 class="absolute font-bold"><a href="#">{{ title }}</a></h3>
    </div>
</template>

<script>
export default {
  props: ['img', 'title']
}
</script>