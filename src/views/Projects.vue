<template>
	<div class="projects">
		<h1 class="title">projects</h1>
		<p class="has-divider has-padding-bottom mb-6">
			Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
			tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim
			veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea
			commodo consequat.
		</p>

		<div v-if="showLinks" class="columns has-text-centered has-padding-top is-desktop">
			<div class="column is-one-third-desktop">
				<i class="fas fa-laptop-code fa-5x"></i>
				<p class="heading">Web Development</p>
				<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
				<router-link to="/projects/code" class="button is-primary mt-4 mb-6">view code</router-link>
			</div>

			<div class="column is-one-third-desktop">
				<i class="fas fa-draw-polygon fa-5x"></i>
				<p class="heading">Graphic Design</p>
				<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
				<router-link to="/projects/designs" class="button is-primary mt-4 mb-6">view designs</router-link>
			</div>

			<div class="column is-one-third-desktop">
				<i class="fas fa-edit fa-5x"></i>
				<p class="heading">Digital Art</p>
				<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</p>
				<router-link to="/projects/art" class="button is-primary mt-4 mb-6">view art</router-link>
			</div>
		</div>

		<router-link v-if="!showLinks" to="/projects">
			<p class="has-text-right mb-2">&#8617; back to projects</p>
		</router-link>

		<router-view></router-view>
	</div>
</template>

<script>
	export default {
		name: 'Projects',
		computed: {
			showLinks() {
				const projects = "projects";
				return this.$route.path.endsWith(projects);
			}
		}
	};
</script>
