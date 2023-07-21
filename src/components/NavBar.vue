<script setup lang="ts">


</script>
<template>
    <nav class="navbar">
        <ul>
            <li><a href=""><span>00</span>Home</a></li>
            <li><a href=""><span>01</span>Destination</a></li>
            <li><a href=""><span>02</span>Crew</a></li>
            <li><a href=""><span>03</span>Technology</a></li>
        </ul>
    </nav>
</template>
<style lang="scss">
nav {
    ul {
        display: flex;
        flex-direction: row;
    }

    li {

        justify-content: space-between;
        list-style-type: none;

        a {
            span {
                margin: 0 1em;
            }

            color: white;
        }
    }

}
</style>
