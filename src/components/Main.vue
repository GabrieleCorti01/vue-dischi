<template>
    <div class="wrapper-container-album">
        <div class="row">
            <div v-for="el in albumList" :key="el.id" class="album-container">
                <AlbumElement :element="el"/>
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
@import '../style/variable.scss';

.row{
    display: flex;
    padding: 50px;
    flex-wrap: wrap;
}

.album-container{
    flex-basis: calc(100% / 5 - 30px);
    background-color: $secondColor;
    margin: 15px;
    padding: 20px;
}


</style>