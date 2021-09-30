<template>
    <div class="wrapper-container-album">
        <div class="row">
            <div class="col-12 element-container" >
                <AlbumElement />
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios';
import AlbumElement from './components/AlbumElement.vue';

export default {
    name: 'Main',
    components : {
        AlbumElement
    },

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