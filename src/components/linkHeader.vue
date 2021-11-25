<template>
    <li>
        <img :src="image" alt="#">
        <a href="#"> {{title}} </a>
    </li>
</template>

<script>
export default {
    props: {
        image: String,
        title:String,
    }
}
</script>

<style>

</style>