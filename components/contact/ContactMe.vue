<template>
        <div class="contact-me">
            <a :href="url" target="__blank">
            <img :src="require(`@/assets/images/${img}`)" height="30">
             <span>{{ name }}</span> </a>
            
            <!-- <h2>{{ name }}</h2> -->
        </div>
</template>

<script>
export default {
    name: "ContactMe",
    props: {
        img: {
            type: String
        },
        name: {
            type: String
        },
        url: {
            type: String
        }
    }
};
</script>

<style scoped>
    @import "@/components/contact/ContactMe.scss";
</style>