<template>
    <div class="w-full sm:w-full md:w-1/3 lg:w-1/3 relative">
        <div class="relative">
            <a href="#">
                <img :src="`/img/${ img }`" :alt="`${ img }`" />
            </a>
        </div>
        <div class=" absolute text-white title-block">
            <h3 class="text-xl">{{ title }}<a href="#"></a></h3>
            <div class="text-xs">
                <span class="font-bold">Cách làm hay</span> - <span>24/3/2021</span>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  props: ['img', 'title']
}
</script>
