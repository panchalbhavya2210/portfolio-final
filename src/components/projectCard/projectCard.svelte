<script>
	import './projectCard.css';
	export let data;
</script>

{#each data as datas}
	<div class="project-card">
		<div class="project-card__wrap">
			<div class="project-card__top">
				<figure>
					<img src="https://picsum.photos/300" alt={datas.projectTitle} />
				</figure>
			</div>
			<div class="project-card__skills">
				{#each datas.projectLanguage as skill}
					<span>{skill}</span>
				{/each}
			</div>
			<div class="project-card__details">
				<h2>{datas.projectTitle}</h2>
				<div class="project-card__desc">{datas.projectDetails}</div>
				<div class="project-card__cta">
					<a href={datas.projectLink} target="_blank" class="primary-btn">Live</a>
				</div>
			</div>
		</div>
	</div>
{/each}
