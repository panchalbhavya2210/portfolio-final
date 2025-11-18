<script>
	import './project.css';
	import ProjectCard from '../../projectCard/projectCard.svelte';
	import RakshitJain from '../../../assets/images/rakshit-jain-portfolio.webp';
	import ElectronEnterprise from '../../../assets/images/electron-enterprise.png';
	const projectData = [
		{
			id: 1,
			projectTitle: "Rakshit Jain's Website",
			projectImage: RakshitJain,
			projectLanguage: ['Svelte', 'HTML', 'GSAP', 'TAILWIND', 'APPWRITE', 'FIREBASE'],
			projectDetails: '',
			projectLink: 'https://rakshit-jain.vercel.app?ref=bhavya-panchal'
		},
		{
			id: 2,
			projectTitle: 'Electron Enterprise',
			projectImage: ElectronEnterprise,
			projectLanguage: ['Next JS', 'HTML', 'SCSS', 'BREVO EMAILS', 'FIREBASE'],
			projectDetails: '',
			projectLink: 'https://electronenterprise.in?ref=bhavya-panchal'
		}
	];
</script>

<section class="projects section-padding">
	<div class="section-header">
		<h2>
			<span>#</span>projects
		</h2>
		<!-- <a href="/project" class="primary-btn"> View all </a> -->
	</div>
	<div class="projects-wrap row">
		<ProjectCard data={projectData} />
	</div>
</section>
