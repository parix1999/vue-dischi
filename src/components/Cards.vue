<template>
    <div>
        {{poster}}
        {{title}}
        {{author}}
        {{year}}

    </div>
</template>


<script>

export default {
    name: 'Cards',
    props: {
        poster: String,
        title: String,
        author: String,
        year: String,
    }
}

</script>



<style lang="scss" scoped>

</style>