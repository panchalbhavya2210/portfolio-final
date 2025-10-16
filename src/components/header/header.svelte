<script>
	import './header.css';
	import Testy from '../../assets/images/test.svg';
	import { onMount, onDestroy } from 'svelte';

	const Links = [
		{
			id: 1,
			linkName: '#home',
			linkTO: '/',
			seoName: 'Home'
		},
		{
			id: 2,
			linkName: '#works',
			linkTO: '/projects',
			seoName: 'Projects'
		},
		{
			id: 3,
			linkName: '#about-me',
			linkTO: '/about-me',
			seoName: 'About Me'
		},
		{
			id: 4,
			linkName: '#contact',
			linkTO: '/contact',
			seoName: 'Contact'
		}
	];

	const socialLinks = [
		{
			id: 1,
			socialIcon: Testy,
			socialIconSeoName: 'Github',
			socialIconLink: 'https://github.com'
		},
		{
			id: 2,
			socialIcon: Testy,
			socialIconSeoName: 'LinkedIn',
			socialIconLink: 'https://github.com'
		},
		{
			id: 3,
			socialIcon: Testy,
			socialIconSeoName: 'Instagram',
			socialIconLink: 'https://github.com'
		}
	];

	let lastScrollY = 0;
	let header;

	function handleScroll() {
		const currentScrollY = window.scrollY;
		if (currentScrollY > lastScrollY) {
			header.style.transform = 'translateY(-100%)';
		} else {
			header.style.transform = 'translateY(0)';
		}
		lastScrollY = currentScrollY;
	}

	onMount(() => {
		header = document.getElementById('ref-head');
		window.addEventListener('scroll', handleScroll, { passive: true });

		// ✅ Handle bfcache safely
		const cleanup = () => {
			window.removeEventListener('scroll', handleScroll);
			document.body.style.overflow = 'auto'; // restore scroll
		};

		// Fired when page goes into bfcache
		window.addEventListener('pagehide', cleanup);
		onDestroy(cleanup);
	});

	let isMenuOpen;

	function openMenu() {
		isMenuOpen = !isMenuOpen;
		if (!isMenuOpen) {
			document.body.style.overflow = 'auto';
		} else {
			document.body.style.overflow = 'hidden';
		}
	}
</script>

<header id="ref-head">
	<div class="container">
		<div class="header-group">
			<div class="header-float sm-hide">
				<div class="header-float__icon">
					{#each socialLinks as socials (socials.id)}
						<a href={socials.socialIconLink} title={socials.socialIconSeoName}>
							<img src={socials.socialIcon} alt="" />
						</a>
					{/each}
				</div>
			</div>
			<div class="header-left">
				<a href="/"> Bhavya </a>
			</div>
			<div class={`hamburger-wrap lg-hide flex ${isMenuOpen ? 'menu-open' : ''}`}>
				<div class="hamburger">
					<button aria-label="menu" on:click={openMenu}></button>
				</div>
			</div>
			<div class="header-links sm-hide">
				<ul>
					{#each Links as LinkData (LinkData.id)}
						<li>
							<a href={LinkData.linkTO || ''} title={LinkData.seoName}>
								<span>
									{LinkData.linkName.charAt(0)}
								</span>
								<span>
									{LinkData.linkName.replace('#', '')}
								</span>
							</a>
						</li>
					{/each}
				</ul>
			</div>
		</div>
	</div>
</header>
<div class={`header-body lg-hide ${isMenuOpen ? 'menu-open' : ''}`}>
	<div class="container">
		<div class="header-links lg-hide">
			<ul>
				{#each Links as LinkData (LinkData.id)}
					<li style={`--i:${LinkData.id}`}>
						<a href={LinkData.linkTO || ''} title={LinkData.seoName}>
							<span>
								{LinkData.linkName.charAt(0)}
							</span>
							<span>
								{LinkData.linkName.replace('#', '')}
							</span>
						</a>
					</li>
				{/each}
			</ul>
		</div>
	</div>
</div>
