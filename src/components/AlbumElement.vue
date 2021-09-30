<template>
  <div>
      <div class="album-box">
          <img :src="element.poster" alt="">
          <h2>{{ element.title.toUpperCase() }}</h2>
          <p class="autore">{{ element.author }}</p>
          <p class="anno">{{ element.year }}</p>
          
      </div>
  </div>
</template>

<script>


export default {
    name: "AlbumElement",
    props: ["element"],


}
</script>

<style scoped lang="scss">
@import '../style/variable.scss';


img{
    width: 100%;
}

h2{
    color: white;
    font-weight: 800;
    padding: 10px 0 20px 0;
}

.autore{
    color: $fontColor;
}

.anno{
    color: $fontColor;
}

</style>
