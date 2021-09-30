<template>
    <section class="container-header">
        <div>
            <i class="fab fa-spotify"></i>
        </div>
    </section>
</template>

<script>
export default {
    name: "Header",
    

}
</script>

<style scoped lang="scss">
@import '../style/variable.scss';

.container-header{
    background-color: $secondColor;
    padding: 20px;
}

i{
    font-size: 4em;
    display: flex;
    color: $logoColor;
}

</style>