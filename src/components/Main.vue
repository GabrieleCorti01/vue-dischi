<template>
    <div class="wrapper-container-album">
        <div class="row">
            <div v-for="(element, index) in albumList" :key="index" class="col-3 album">

            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios';

export default {
    name: 'Main',

    data: function(){
       return {
           albumList: []
       }
    },
    created: function(){
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((risposta) => {
            this.albumList = risposta.data.results.slice();
            console.log(this.albumList)
        })
    }
    
}

</script>

<style scoped lang="scss">

</style>