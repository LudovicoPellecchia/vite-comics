<script>
export default {
    props: {
        imgSrc: String,
        title: String,
    }


}
</script>

<template>
    <div class="card border-0">
        <img :src="imgSrc" class="card-img-top rounded-0" alt="...">
        <h5>{{ title.toUpperCase() }}</h5>
    </div>
</template>


<style lang="scss" scoped>
.card{
    background-color:  #1C1C1C;
}

img {
    aspect-ratio: 1/1;
    object-fit: cover;
    object-position: top;
}

h5{
    font-size: 1.2rem;
    font-weight: 300;
    padding-top: 15px;
    color: white;
}
</style>