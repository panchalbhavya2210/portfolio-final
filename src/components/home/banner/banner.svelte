<script>
	import './banner.css';
	import MazePath from '../../../assets/images/maze-path.svg';
</script>

<section class="banner">
	<div class="banner-wrap">
		<div class="banner-wrap__left">
			<h1>
				Bhavya is a <span>web designer</span> and <span>front-end developer</span>
			</h1>
			<div class="banner-wrap__desc">
				<p>He crafts responsive websites where technologies meet creativity</p>
			</div>
			<div class="banner-wrap__cta">
				<a href="/contact-me" class="primary-btn">Contact me</a>
			</div>
		</div>
		<div class="banner-wrap__right">
			<span class="center-dot"></span>
			<img
				src={MazePath}
				alt="maze"
				loading="eager"
				fetchpriority="high"
				width="410"
				height="410"
			/>
			<span class="connector"></span>
		</div>
		<div class="seo-only">
			<p>Currently working at eQuest Solutions.</p>
		</div>
	</div>
</section>
