<template>
  <div class="container">
    <div class="intro">
		<h1 class="project__title">
			Hi, I'm Oluwadara. <br>
			I am a Software Developer. <br>
		</h1>
	</div> <hr>
	<div id="projects">
		<h1 class="title">Projects</h1>
		<div class="project__cards">
			<ProjectCard v-for="project in projects" :key="project.id" :name=project.name :desc=project.desc :img=project.img :url=project.url></ProjectCard>
		</div>
		<div class="project__btn">
		<Button buttonIcon="arrow-right" buttonName="See All Other Projects" btnLink="/projects"/> <hr>
		</div>
	</div>

	<h1 class="title">Interests</h1>
	<div id="interests" class="interests">	
		<Interests v-for="interest in interests" :key="interest.id" :name=interest.name :img=interest.img></Interests>
	</div> <hr>
	<div id="contact-me">
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
