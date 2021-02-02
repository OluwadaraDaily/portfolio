<template>
       <div class="project__card">
			<img :src="require(`@/assets/images/${img}`)" height="200">
			<h1 class="project__title">{{ name }}</h1>
			<p class="project__desc">
				{{ desc }}
				<br> <br> Check it out <a :href="url"  target="_blank"><b>here.</b></a>
			</p>
		</div> 
</template>

<script>
export default {
    name: "ProjectCard",
    props: {
        url: {
			type: String
		},
		img: {
			type: String
		},
		name: {
			type: String,
		},
		desc: {
			type: String
		}
    }
};
</script>

<style>
	@import "@/components/ProjectCard.scss";
</style>