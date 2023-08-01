<script setup lang="ts">
    import { ref } from 'vue';
    let toggle = ref(false)
    
    function menuToggle(){
        toggle.value = !toggle.value
        
    }
</script>
<template>
    <nav class="navbar" role="navigation" aria-expanded="false">
        <ul class="menu" :class="{expand: toggle}">
            <li><a href="" class="nav-text"><span class="bold">00</span>Home</a></li>
            <li><a href="" class="nav-text"><span class="bold">01</span>Destination</a></li>
            <li><a href="" class="nav-text"><span class="bold">02</span>Crew</a></li>
            
            <li><a href="" class="nav-text"><span class="bold">03</span>Technology</a></li>
        </ul>
        <button  id="hamburger" @click="menuToggle"><span class="hidden-but-accessible">Menu</span></button>
        
    </nav>
</template>
<style  lang="sass">
nav 
    min-height: 4em
    width: 100vw
    display: flex
    // input
    //     opacity: 0
    //     z-index: 0
    //     padding: 0
    //     top: 3.5em
    //     right: 2.2em
    //     display: block
    //     position: absolute
    ul 
        display: flex
        flex-direction: column
        padding: 0
    li 
        list-style-type: none
        margin: .5em auto .5em 0
    a 
        span 
            margin: 0 1em
      
        color: white
        -webkit-transition: color 0.3s ease
        -o-transition: color 0.3s ease
        transition: color 0.3s ease
    a:hover
        color: #D0D6F9
    button
        border: none
        background: url('../assets/icon-hamburger.svg')
        border-radius: 0px
        height: 1.3em
        width: 1.7em
        padding: 0
        margin: auto 2em auto auto
        display: block
        position: relative
        z-index: 1
        -webkit-user-select: none
        -moz-user-select: none
        -ms-user-select: none
        user-select: none
    .menu
        position: absolute
        background: #0B0D17
        width: 300px
        margin: -100px 0 0 -50px
        padding: 50px
        padding-top: 125px
        height: 100vh
        list-style-type: none
        /* Hide the menu off-screen to the left */
        right: -100%
        -webkit-transition: right 0.3s ease
        -o-transition: right 0.3s ease
        transition: right 0.3s ease
    .expand
        right: 0


@media only screen and (min-width: 768px)
        nav 
            ul
                flex-direction: row
            li
                margin: auto auto auto 0
        
    
@media only screen and (min-width: 992px) 
    #hamburger
        display: none
    
        
    
</style>
