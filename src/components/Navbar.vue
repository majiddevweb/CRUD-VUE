<!--
// By majiddevweb 
// @BENHAROUN TV
// Creative solution specializing in Web Design, Motion Graphics, Video editing, VFX.

// KhaLi 
-->

<template>
    <nav class="navbar" role="navigation" aria-label="main navigation">
    <div class="navbar-brand">
        <a class="navbar-item">
        <img src="./logo.png" width="40" height="120">
        </a>
    </div>

    <div class="navbar-menu">
            <div class="navbar-start">
                <a v-for="link in links" :key="link.title" class="navbar-item" @click="$router.push(link.url)">
                    {{link.title}}
                </a>
        </div>

        <div class="navbar-end">
            <div class="navbar-item">
                <div class="buttons">
                <a class="button is-primary" @click="goToMySite()">
                    <strong>Made by BENHAROUN TV</strong>
                </a>
                </div>
            </div>
        </div>
    </div>
    </nav>
</template>

<script>
export default {
    name:'Navbar',
    props:['links'],
    methods: {
        goToMySite: () => window.open('https://www.instagram.com/benharoun_tv/', '_blank')
    }
}   

</script>
<style scoped>
a.navbar-item {
    text-transform:capitalize;
    }
</style>
