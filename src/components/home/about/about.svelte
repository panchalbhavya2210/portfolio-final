<script>
	import './about.css';
	import PillImage from '../../../assets/images/pill-image.webp';
</script>

<section class="about section-padding">
	<div class="section-header">
		<h2><span>#</span>about-me</h2>
	</div>
	<div class="about-wrap row">
		<div class="about-wrap__left">
			<p>
				Hello, i’m Bhavya!
				<br />
				<br />
				I’m a self-taught front-end developer based in Gujarat, India. I can develop responsive websites
				from scratch and raise them into modern user-friendly web experiences.
				<br />
				<br />
				Transforming my creativity and knowledge into a websites has been my passion for over a year.
				I have been helping various clients to establish their presence online. I always strive to learn
				about the newest technologies and frameworks.
			</p>
			<div class="cta">
				<a href="#contact" class="primary-btn" title="contact"> Contact Me </a>
			</div>
		</div>
		<div class="about-wrap__right">
			<img src={PillImage} alt="" />
		</div>
	</div>
</section>
