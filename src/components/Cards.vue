<template>
    <div class="bg-cards">
        <div class="inner">
            <div class="box-pic-song">
                <!-- Ricorda il blind, perchè lo stai prendendo come dato il link della immagine: -->
                <img :src="poster" alt="'link è:' + title">
            </div>

            <div class="titolo">
                {{title}}
            </div>

            <div class="autore">
                {{author}}
            </div>

            <div class="anno">
                {{year}}
            </div>

        </div>

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

    .bg-cards {
        background: #2e3a46;

    }
    .box-pic-song {
        width:200px;
        img {
            width:100%;
        }
    }



</style>