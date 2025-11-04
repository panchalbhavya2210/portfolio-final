<script>
	import './project.css';
	import ProjectCard from '../../projectCard/projectCard.svelte';

	const projectData = [
		{
			id: 1,
			projectTitle: 'Portfolio',
			projectLanguage: ['Svelte', 'HTML', 'GSAP', 'TAILWIND', 'APPWRITE', 'FIREBASE'],
			projectDetails: 'Lorem*10',
			projectLink: 'https://rakshit-jain.vercel.app?ref=bhavya'
		},
		{
			id: 2,
			projectTitle: 'Landing Page',
			projectLanguage: ['Next JS', 'HTML', 'SCSS', 'BREVO EMAILS', 'FIREBASE'],
			projectDetails: 'Lorem*10',
			projectLink: 'https://electronenterprise.in'
		},
		{
			id: 3,
			projectTitle: 'Landing Page',
			projectLanguage: ['Next JS', 'HTML', 'SCSS', 'BREVO EMAILS', 'FIREBASE'],
			projectDetails: 'Lorem*10',
			projectLink: 'https://electronenterprise.in'
		}
	];
</script>

<section class="projects">
	<div class="section-header">
		<h2>
			<span>#</span>projects
		</h2>
		<a href="/project" class="primary-btn"> View all </a>
	</div>
	<div class="projects-wrap">
		<ProjectCard data={projectData} />
	</div>
</section>
