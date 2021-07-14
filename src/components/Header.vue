<template>
    <div class="bg-header">
        <div class="box-logo">
            <img src="../assets/spotify-logo.png" alt="logo-spotify">
        </div>
    </div>
</template>


<script>

export default {
    name: 'Header',
}

</script>



<style lang="scss" scoped>

    .bg-header {
        background-color: #2e3a46;
        padding:15px;
        margin-bottom: 50px;


        .box-logo {
            width:70px;
            img {
                width:100%;
            }
        }
    }


</style>
