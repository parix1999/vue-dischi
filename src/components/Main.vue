<template>
    <div>
        <Cards />
    </div>
</template>


<script>

import Cards from './Cards.vue'

export default {
    name: 'Main',
    components:{
        Cards,
    },
    props: {
        albums: Array,
    }
}

</script>



<style lang="scss" scoped>

</style>