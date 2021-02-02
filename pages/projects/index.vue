<template>
    <div>
		<h1 class="title">Projects</h1>
		<div class="project__cards">
        <ProjectCard v-for="project in projects" :key="project.id" :name=project.name :desc=project.desc :img=project.img :url=project.url></ProjectCard>
		</div>
    </div>    
</template>

<script>
export default {
    data () {
        return {
            projects: [
				{
					name: "Dad Jokes",
					url: 'http://deadjokes.netlify.app',
					img: 'dad-jokes.jpg',
					desc: "This is a website where you can get nice dad jokes.You can also send jokes to someone's mail."
				},
				{
					name: "Message County",
					url: 'http://message-county.herokuapp.com',
					img: 'message-county.svg',
					desc: "This is a website where you can sned instant messages to groups that you create. It was built with Flask, Javascript and Socket IO."
				},
				{
					name: "Pizza Mange",
					url: 'http://pizza-mange.herokuapp.com',
					img: 'pizza-mange.jpg',
					desc: "This is a pizza-ordering website, utilising the Menu of Pinocchio's at Harvard. It was developed with Django, Javascript, and SQLite3. "
				},
				{
					name: "Productify App",
					url: 'http://productify-app.netlify.app/',
					img: 'productify.jpg',
					desc: "This is a store where items can be added to a cart. The REST API for this project was developed with AdonisJS while the front end was developed with VueJS, utiliing Vuex for storing cart data and authentication."
				},
				{
					name: "Dailypedia",
					url: 'http://daily-pedia.herokuapp.com/',
					img: 'dailypedia.jpg',
					desc: "This is a private encyclopedia where you can add enteries, get certain enteries, search for enteries, and get random enteries. This project was developed with Django."
				},
				{
					name: "Pondify",
					url: 'http://pondify.herokuapp.com/',
					img: 'pondify.jpg',
					desc: "This is an app for getting real time data from your pond connected to your ThingSpeak account. I made this for my final year project."
				},
				

			],
        }
    }
}
</script>

<style scoped>
	@media only screen and ( min-width: 800px ) {
		.project__cards {
			display: flex;
			flex-wrap: wrap;
        	flex-direction: row;
        	justify-content: space-around;
		}
		.project__cards > div {
			margin: 15px 10px;
		}
	}
</style>