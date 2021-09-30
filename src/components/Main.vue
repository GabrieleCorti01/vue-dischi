<template>
    <div class="wrapper-container-album">
        <div class="row">
            <div v-for="element in albumList" :key="element.id">
                <AlbumElement :title="element.author"/>
            </div>
        </div>
    </div>
</template>

<script>

import AlbumElement from './AlbumElement.vue';
import axios from 'axios';

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
        this.albumList = risposta.data.response.slice();
        console.log(this.albumList)
        
    })
}

    
}

</script>

<style scoped lang="scss">

</style>