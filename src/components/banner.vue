<template>
    <div class="banner-top" >
        <p>{{ titre }}</p>
    </div>
</template>

<script>


export default {
    name: 'banner',
    data() {
        return {
            titre: 'La todo liste',
        } 
    },
}
</script>

<style scoped>

.banner-top {
    position: fixed;
    top: 0;
    height: 50px;
    background: #333;
    color: #f1f1f1;
    width: 100%;
    text-align: center;
    line-height: 50px;
    font-size: 25;
}

</style>
