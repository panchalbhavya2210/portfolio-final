<script>
	import './skills.css';
	import SkillsImage from '../../../assets/images/skills-bg.webp';

	const SkillGroups = [
		{
			title: 'Languages',
			items: ['Javascript', 'Python']
		},
		{
			title: 'Databases',
			items: ['Firebase', 'Supabase', 'AppWrite']
		},
		{
			title: 'Other',
			items: ['HTML', 'CSS', 'SCSS', 'Tailwind CSS', 'Material UI']
		},
		{
			title: 'Tools',
			items: ['VSCode', 'Linux (Ubuntu, Mint)', 'Git', 'Figma']
		},
		{
			title: 'Frameworks',
			items: ['React JS', 'Next JS', 'Svelte', 'Vue', 'Nuxt JS']
		}
	];
</script>

<section class="skills section-padding">
	<div class="section-header">
		<h2><span>#</span>skills</h2>
	</div>

	<div class="row">
		<div class="skills-left">
			<img src={SkillsImage} loading="lazy" alt="skills-background" />
		</div>

		<div class="skills-right">
			<div class="skills-card">
				{#each SkillGroups as group, i (i)}
					<div class="skills-card__inner">
						<div class="skills-card__wrapper">
							<div class="skills-card__header">
								<h3>{group.title}</h3>
							</div>

							<div class="skills-card__skills project-card__skills">
								{#each group.items as item, i (i)}
									<span>{item}</span>
								{/each}
							</div>
						</div>
					</div>
				{/each}
			</div>
		</div>
	</div>
</section>
