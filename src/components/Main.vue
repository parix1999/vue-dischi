<template>
    <div class="row">
        <Cards v-for="(card, index) in albums" :key="index"
        :poster="card.poster"
        :title="card.title"
        :author="card.author"
        :year="card.year"/>
            

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