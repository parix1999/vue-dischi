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
        width: calc(100% / 5);
        text-align: center;
        .inner {
            background: #2e3a46;
            height:400px;
            margin-top:24px;
            padding: 15px;
        }
    }
    .box-pic-song {
        width:200px;
        margin:0 auto;
        img {
            width:100%;
        }
    }
    .titolo {
        color:white;
        font-size: 30px;
        font-weight: bold;
    }
    .autore{
        color: #7e8080;
    }
    .anno{
        color: #7e8080;
    }


</style>