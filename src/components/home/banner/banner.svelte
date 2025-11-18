<script>
	import './banner.css';
	import MazePath from '../../../assets/images/maze-path.svg';
	import MyImage from '../../../assets/images/pill-image.webp';
</script>

<section class="banner">
	<div class="banner-wrap">
		<div class="banner-wrap__left">
			<h1>I Am Bhavya Panchal, A <span>Web</span> Developer.</h1>
			<div class="banner-wrap__desc">
				<p>
					A web developer and UI designer who loves turning ideas into reality. I'm always looking
					for ways to improve and grow in my craft!
				</p>
			</div>
			<div class="banner-wrap__cta">
				<a href="#contact" class="primary-btn">Contact me</a>
			</div>
		</div>
		<div class="banner-wrap__right">
			<span class="center-dot"></span>
			<img src={MyImage} alt="maze" loading="eager" fetchpriority="high" width="410" height="410" />
			<span class="connector"></span>
		</div>
		<div class="seo-only">
			<p>Open to work</p>
		</div>
	</div>
</section>
