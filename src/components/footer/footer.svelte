<script>
	import './footer.css';

	import MailIcon from '../../assets/images/gmail-svg.svg';
	import LinkedInIcon from '../../assets/images/linkedin-svg.svg';
	import GitIcon from '../../assets/images/test.svg';
	import Instagram from '../../assets/images/instagram-svg.svg';

	const SocialLinks = [
		{
			icon: MailIcon,
			link: 'mailto:panchalbhavya2210@gmail.com',
			linkName: '@panchalbhavya2210'
		},
		{
			icon: LinkedInIcon,
			link: 'https://linkedin.com/in/bhavyapanchal',
			linkName: 'Linkedin'
		},
		{
			icon: GitIcon,
			link: 'https://github.com/panchalbhavya2210',
			linkName: 'Github'
		},
		{
			icon: Instagram,
			link: 'https://instagram.com',
			linkName: '@bhavya_2210'
		}
	];
</script>

<footer class="footer">
	<div class="container">
		<div class="footer-top">
			<div class="footer-top__left">
				<div class="footer-top__head">
					<a href="/" title="Home">Bhavya</a>
					<a
						href="mailto:panchalbhavya2210@gmail.com"
						target="_blank"
						rel="noopener noreferrar"
						title="Mail Me"
						class="secondary-link"
					>
						@panchalbhavya2210
					</a>
				</div>
				<div class="footer-top__desc">
					<p>Web designer and front-end developer</p>
				</div>
			</div>
			<div class="footer-top__right">
				<h4>Links</h4>
				<div class="footer-link__cont">
					{#each SocialLinks as Link, i (i)}
						<a href={Link.link} target="_blank" title={Link.linkName} rel="noopener noreferrar">
							<img src={Link.icon} alt="" />
						</a>
					{/each}
				</div>
			</div>
		</div>
		<div class="footer-bottom">
			<div class="footer-bottom__copyright-me">
				<p>
					Thanks to <a
						href="https://eliasdevis.github.io"
						target="_blank"
						rel="noopener noreferrar"
						title="Credits where due">Elias Dev</a
					> for Design
				</p>
			</div>
		</div>
	</div>
</footer>
