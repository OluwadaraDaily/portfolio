<template>
        <div class="interest">
            <img :src="require(`@/assets/images/${img}`)" height="100">
            <h1 class="interest__title"> {{ name }} </h1>
        </div>
</template>

<script>
export default {
    name: "Interests",
    props: {
        img: {
            type: String
        },
        name: {
            type: String
        }
    }
    
};
</script>

<style scoped>
    @import "@/components/interests/Interests.scss";
</style>