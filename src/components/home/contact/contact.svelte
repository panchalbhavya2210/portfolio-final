<script>
	import './contact.css';

	import MailIcon from '../../../assets/images/gmail-svg.svg';
	import LinkedInIcon from '../../../assets/images/linkedin-svg.svg';

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
		}
	];
</script>

<section class="contact section-padding" id="contact">
	<div class="section-header">
		<h2><span>#</span>contact</h2>
	</div>
	<div class="contact-wrap row">
		<div class="contact-wrap__left">
			<p>
				I’m interested in fulltime opportunities. However, if you have other request or question,
				don’t hesitate to contact me
			</p>
		</div>
		<div class="contact-wrap__right">
			<div class="contact-wrap__box">
				<div class="contact-wrap__header">
					<h3>Message me here</h3>
				</div>
				<div class="contact-wrap__links">
					{#each SocialLinks as socials, i (i)}
						<a
							href={socials.link}
							title={socials.linkName}
							class="links"
							target="_blank"
							rel="noopener noreferrer"
						>
							<div class="icon">
								<img src={socials.icon} alt="" />
							</div>
							<div class="link">
								<p>{socials.linkName}</p>
							</div>
						</a>
					{/each}
				</div>
			</div>
		</div>
	</div>
</section>
