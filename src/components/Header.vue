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

        <div class="selezione">
            <label for="genere">Choose a genere:</label>

            <select v-model="choice" name="genere" id="scelta">
                <option >Rock</option>
                <option >pop</option>
                <option >metal</option>
                <option >jazz</option>

            </select>
            <button @click="$emit('cerca', choice)">
                Search
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
            choice: '',
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

    .selezione {
        margin-left:20px;
        color:white;
    }
  


</style>
