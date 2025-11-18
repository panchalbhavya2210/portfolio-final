<script>
	import './projectCard.css';
	export let data;

	let loaded = {}; // track load state for each image

	const handleLoad = (id) => {
		loaded[id] = true;
		loaded = { ...loaded };
	};
</script>

{#each data as datas, i}
	<div class="project-card" key={i}>
		<div class="project-card__wrap">
			<div class="project-card__top">
				<figure>
					<img
						src={datas.projectImage + '?blur=10&size=20'}
						alt={datas.projectTitle}
						class:hide={loaded[datas.id]}
						class="lqip"
						loading="lazy"
					/>
					<div class="loader" class:hide={loaded[datas.id]}></div>
					<img
						src={datas.projectImage}
						alt={datas.projectTitle}
						on:load={() => handleLoad(datas.id)}
						class:show={loaded[datas.id]}
						class="hq"
						loading="lazy"
					/>
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

<style>
	figure {
		position: relative;
		overflow: hidden;
	}

	.lqip,
	.hq {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		object-fit: cover;
		transition: opacity 0.3s ease;
	}

	.hide {
		opacity: 0;
	}

	.show {
		opacity: 1;
	}

	/* Loader */
	.loader {
		position: absolute;
		top: 50%;
		left: 50%;
		width: 32px;
		height: 32px;
		transform: translate(-50%, -50%);
		border: 3px solid #ccc;
		border-top-color: var(--primary-color);
		border-radius: 50%;
		animation: spin 0.7s linear infinite;
	}

	.hide.loader {
		opacity: 0;
	}

	@keyframes spin {
		from {
			transform: translate(-50%, -50%) rotate(0deg);
		}
		to {
			transform: translate(-50%, -50%) rotate(360deg);
		}
	}
</style>
