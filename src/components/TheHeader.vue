<script>
export default {
    data(){
        return{
            navLinks: [
            {name: "Characters"},
            {name: "Comics"},
            {name: "Movies"},
            {name: "TV"},
            {name: "Games"},
            {name: "Collectibles"},
            {name: "Videos"},
            {name: "Fans"},
            {name: "News"},
            {name: "Shop"},
        ]
        }
    }
}
</script>

<template>
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container d-flex">
            <div class="img-wrapper">
                <img src="../assets/img/dc-logo.png" alt="">
            </div>
            <div class="navlink-wrapper">
                <div class="collapse navbar-collapse" id="navbarNav">
                    <ul class="navbar-nav" >
                        <li class="nav-item" v-for="link in navLinks">
                            <a class="nav-link" href="#">{{link.name}}</a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </nav>
</template>

<style lang="scss" scoped>
nav{
    padding: 1rem 0px;
}
</style>
