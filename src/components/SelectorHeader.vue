<template>
  <div class="selector-container">
      <form action="">
          <label for="cars">Choose a genre:</label>
            <select name="cars" id="cars">
                <option value="volvo">Volvo</option>
            </select>
      </form>
  </div>
</template>

<script>
export default {
    name: "SelectorHeader",
}
</script>

<style scoped lang="scss">
@import '../style/variable.scss';

</style>