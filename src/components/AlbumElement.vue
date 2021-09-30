<template>
  <div>
      <div>
          <img :src="img" alt=""> 
      </div>
  </div>
</template>

<script>


export default {
    name: "AlbumElement",
    props: ["img", "title"],


}
</script>

<style scoped lang="scss">

</style>