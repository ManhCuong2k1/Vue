<template>
    <div class="country w-full sm:w-full md:w-1/5 lg:w-1/5">
        <h3>{{ country }}</h3>
        <p>{{ number }}</p>
        <span class="state">{{ text }}</span>
        <span class="update">Updated on 31/03/2021 17:55</span>
    </div>
</template>

<script>
export default {
  props: ['country', 'number', 'text']
}
</script>
