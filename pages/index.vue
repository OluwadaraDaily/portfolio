<template>
  <div class="container">
    <div class="intro">
		<h1 class="project__title">
			Hi, I'm Oluwadara. <br>
			I am a Software Developer. <br>
		</h1>
	</div>
	<div id="projects" class="projects">
		<h1 class="title">Projects</h1>
		<div class="project__cards">
			<ProjectCard v-for="project in projects" :key="project.id" :name=project.name :desc=project.desc :img=project.img :url=project.url></ProjectCard>
		</div>
		<div class="project__btn">
		<Button buttonIcon="arrow-right" buttonName="See All Other Projects" btnLink="/projects"/>
		</div>
	</div> 

	<div class="interest-wrapper">
		<h1 class="title">Interests</h1>
		<div id="interests" class="interests">	
			<Interests v-for="interest in interests" :key="interest.id" :name=interest.name :img=interest.img></Interests>
		</div>
	</div>
	<div id="contact-me" class="contact-me">
		<h1 class="title">Contact Me</h1>
		<ContactMe v-for="contact in contacts" :key=contact.id :img=contact.img :name=contact.name :url=contact.url></ContactMe>
	</div>
  </div>
</template>

<script>
import Interests from '../components/interests/Interests'
import ProjectCard from "../components/ProjectCard"
import Button from "../components/button/Button"
import ContactMe from "../components/contact/ContactMe"
export default {
	data() {
		return {
			projects: [
				{
					name: "Pondify",
					url: 'http://pondify.herokuapp.com/',
					img: 'pondify.jpg',
					desc: "This is an app for getting real time data from your pond connected to your ThingSpeak account. I made this for my final year project."
				},
				{
					name: "Pizza Mange",
					url: 'http://pizza-mange.herokuapp.com',
					img: 'pizza-mange.jpg',
					desc: "This is a pizza-ordering website, utilising the Menu of Pinocchio's at Harvard. It was developed with Django, Javascript, and SQLite3. "
				},
				

			],
			interests: [
				{
					img: 'web-dev.svg',
					name: "Web Development"
				},
				{
					img: 'iot.svg',
					name: "Internet of Things (IoT)"
				},
				{
					img: 'gaming.svg',
					name: "Video Games"
				}
			],
			contacts: [
				{
					img: "instagram.svg",
					name: "chroniclesofdara",
					url: "https://www.instagram.com/chroniclesofdara"
				},
				{
					img: "twitter.svg",
					name: "OluwadaraDaily",
					url: "https://www.twitter.com/oluwadaradaily"
				},
				{
					img: "whatsapp.svg",
					name: "08101217017",
					url: "tel:08101217017"
				},
				{
					img: "email.svg",
					name: "Send me a mail",
					url: "mailto:daraoloye99@gmail.com"
				}
			]
		}
	},
	components: {
		ProjectCard,
		Button,
		ContactMe,
		Interests
	}
};
</script>

<style>
	 @import url('../assets/css/index.scss');
</style>
