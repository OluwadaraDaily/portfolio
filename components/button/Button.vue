<template>
       <div class="btn">
           <router-link :to="btnLink">{{ buttonName }}</router-link>
           <font-awesome-icon 
           v-if="buttonIcon != null"
           class="icon"
           :icon="['fa', buttonIcon]"
           >
           </font-awesome-icon>
		</div> 
</template>

<script>
export default {
    name: "Button",
    props: {
        btnLink: {
            type: String,
            default: "#"
        },
        buttonIcon: {
            type: String
        },
        buttonName: {
            type: String
        }
    }
};
</script>

<style>
	@import "@/components/button/Button.scss";
</style>