<template>
    <div class="bg-header">
        <div class="box-logo">
            <img src="../assets/spotify-logo.png" alt="logo-spotify">
        </div>
        <div class="interazione">
            <input type="text" placeholder="prova"
            v-model="searchString">
            <button @click="$emit('search', searchString)">
                Prova
            </button>
        </div>
    </div>
</template>


<script>

export default {
    name: 'Header',
    data: function() {
        return {
            searchString:'',
        }
    }
}

</script>



<style lang="scss" scoped>

    .bg-header {
        background-color: #2e3a46;
        padding:15px;
        display:flex;
        align-items: center;


        .box-logo {
            width:70px;
            img {
                width:100%;
            }
        }
    }

    .interazione {
        margin-left:20px;
    }
  


</style>
