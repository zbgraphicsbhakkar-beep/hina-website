<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta name="description" content="Hina Tabbasum is a multidisciplinary designer crafting thoughtful identities, digital experiences, and visual stories.">
	<title>Hina Tabbasum — Designer & Visual Storyteller</title>
	<link rel="preconnect" href="https://fonts.googleapis.com">
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
	<link href="https://fonts.googleapis.com/css2?family=DM+Mono:wght@400;500&family=Manrope:wght@400;500;600;700;800&family=Playfair+Display:ital,wght@0,600;1,600&display=swap" rel="stylesheet">
	<style>
		:root {
			--ink: #17211f;
			--muted: #66716c;
			--paper: #f5f1e9;
			--card: #e8eee6;
			--coral: #e96f54;
			--yellow: #f3c969;
			--line: rgba(23, 33, 31, .16);
			--serif: "Playfair Display", Georgia, serif;
			--sans: "Manrope", sans-serif;
			--mono: "DM Mono", monospace;
		}

		* { box-sizing: border-box; }
		html { scroll-behavior: smooth; }
		body { margin: 0; color: var(--ink); background: var(--paper); font-family: var(--sans); }
		a { color: inherit; text-decoration: none; }
		.wrap { width: min(1160px, calc(100% - 64px)); margin: auto; }
		.eyebrow { color: var(--coral); font: 500 11px var(--mono); letter-spacing: .08em; text-transform: uppercase; }

		header { padding: 26px 0; position: relative; z-index: 2; }
		nav { display: flex; align-items: center; justify-content: space-between; }
		.brand { font-weight: 800; letter-spacing: -.07em; font-size: 22px; }
		.brand span { color: var(--coral); }
		.nav-links { display: flex; gap: 34px; font-size: 13px; font-weight: 600; }
		.nav-links a { transition: color .2s; }
		.nav-links a:hover { color: var(--coral); }
		.nav-cta { border-bottom: 1px solid var(--ink); padding-bottom: 4px; font-size: 13px; font-weight: 700; }

		.hero { min-height: 675px; display: grid; grid-template-columns: 1.08fr .92fr; gap: 50px; align-items: center; padding: 55px 0 100px; }
		.hero-copy h1 { font-size: clamp(56px, 8vw, 102px); line-height: .94; letter-spacing: -.085em; margin: 18px 0 28px; max-width: 670px; }
		.hero-copy h1 em { color: var(--coral); font-family: var(--serif); font-weight: 600; letter-spacing: -.07em; }
		.hero-copy p { color: var(--muted); font-size: 16px; line-height: 1.7; max-width: 405px; margin: 0 0 33px; }
		.button { display: inline-flex; align-items: center; gap: 18px; background: var(--ink); color: var(--paper); padding: 15px 20px; font-size: 12px; font-weight: 700; }
		.button .arrow { font-size: 18px; line-height: 0; transition: transform .2s; }
		.button:hover .arrow { transform: translate(4px, -4px); }

		.hero-art { min-height: 475px; position: relative; display: grid; place-items: center; }
		.hero-art::before { content: ""; position: absolute; width: 88%; aspect-ratio: 1; border-radius: 50%; background: var(--yellow); right: 0; top: 7%; }
		.hero-art::after { content: "H T"; position: absolute; font: italic 600 180px var(--serif); color: var(--coral); transform: rotate(-14deg); opacity: .9; top: 22%; left: 4%; z-index: 1; }
		.portrait { width: 72%; aspect-ratio: .72; object-fit: cover; filter: saturate(.82); position: relative; z-index: 2; mix-blend-mode: multiply; }
		.art-note { position: absolute; right: 4%; bottom: 9%; z-index: 3; background: var(--paper); padding: 12px 14px; font: 10px var(--mono); line-height: 1.5; transform: rotate(6deg); }

		.ticker { border-top: 1px solid var(--ink); border-bottom: 1px solid var(--ink); overflow: hidden; white-space: nowrap; padding: 13px 0; }
		.ticker-track { display: inline-flex; gap: 30px; animation: slide 22s linear infinite; font: 11px var(--mono); text-transform: uppercase; letter-spacing: .08em; }
		.ticker b { color: var(--coral); font-weight: 400; }
		@keyframes slide { to { transform: translateX(-30%); } }

		.intro { padding: 130px 0 115px; display: grid; grid-template-columns: .55fr 1fr; gap: 80px; }
		.intro h2 { font-size: clamp(34px, 4vw, 53px); line-height: 1.05; letter-spacing: -.07em; margin: 0; max-width: 620px; }
		.intro h2 em { font-family: var(--serif); color: var(--coral); font-weight: 600; }
		.intro-copy { border-left: 1px solid var(--line); padding-left: 38px; }
		.intro-copy p { color: var(--muted); line-height: 1.8; max-width: 490px; margin: 0 0 28px; }
		.text-link { display: inline-block; font-size: 12px; font-weight: 800; border-bottom: 1px solid var(--coral); padding-bottom: 6px; }

		.work { background: var(--ink); color: var(--paper); padding: 100px 0 125px; }
		.work-head { display: flex; align-items: end; justify-content: space-between; margin-bottom: 46px; }
		.work h2 { font-size: clamp(40px, 5vw, 64px); letter-spacing: -.075em; margin: 14px 0 0; }
		.work-head p { color: #a9b1aa; font-size: 13px; max-width: 205px; line-height: 1.6; margin: 0; }
		.projects { display: grid; grid-template-columns: 1fr 1fr; gap: 22px; }
		.project { display: block; }
		.project:nth-child(2) { margin-top: 100px; }
		.project:nth-child(3) { margin-top: -30px; }
		.project-image { aspect-ratio: 1.23; overflow: hidden; background: var(--card); }
		.project-image img { width: 100%; height: 100%; object-fit: cover; transition: transform .5s ease; }
		.project:hover img { transform: scale(1.04); }
		.project:nth-child(2) .project-image img { filter: saturate(.7); }
		.project-info { display: flex; justify-content: space-between; gap: 20px; padding: 17px 0; border-bottom: 1px solid rgba(245,241,233,.25); }
		.project-info h3 { font-size: 17px; margin: 0 0 5px; letter-spacing: -.04em; }
		.project-info p { color: #a9b1aa; font: 10px var(--mono); margin: 0; text-transform: uppercase; }
		.project-info span { color: var(--yellow); font-size: 19px; }

		.contact { padding: 120px 0 110px; display: grid; grid-template-columns: .45fr 1fr; gap: 80px; }
		.contact h2 { font-size: clamp(45px, 7vw, 88px); line-height: .93; letter-spacing: -.09em; margin: 14px 0 30px; }
		.contact h2 em { color: var(--coral); font-family: var(--serif); font-weight: 600; }
		.contact-main { border-top: 1px solid var(--ink); padding-top: 27px; }
		.contact-main p { color: var(--muted); line-height: 1.75; max-width: 405px; margin: 0 0 30px; }
		.email { font: 600 clamp(20px, 3vw, 34px) var(--sans); letter-spacing: -.06em; border-bottom: 2px solid var(--coral); padding-bottom: 7px; }
		footer { border-top: 1px solid var(--line); padding: 22px 0; display: flex; justify-content: space-between; color: var(--muted); font: 10px var(--mono); text-transform: uppercase; }
		.socials { display: flex; gap: 25px; color: var(--ink); }

		@media (max-width: 700px) {
			.wrap { width: min(100% - 38px, 550px); }
			.nav-links { display: none; }
			.hero { display: block; min-height: auto; padding: 55px 0 72px; }
			.hero-copy h1 { font-size: clamp(54px, 16vw, 88px); }
			.hero-art { min-height: 350px; margin-top: 40px; }
			.hero-art::after { font-size: 125px; }
			.intro, .contact { display: block; padding: 85px 0; }
			.intro-copy { margin-top: 38px; padding: 27px 0 0; border-left: 0; border-top: 1px solid var(--line); }
			.work { padding: 75px 0 85px; }
			.work-head { display: block; }
			.work-head p { margin-top: 20px; }
			.projects { display: block; }
			.project, .project:nth-child(2), .project:nth-child(3) { margin: 0 0 45px; }
			.contact-main { margin-top: 50px; }
			.email { display: inline-block; font-size: 20px; }
			footer { gap: 16px; flex-wrap: wrap; }
		}
	</style>
</head>
<body>
	<header>
		<nav class="wrap">
			<a class="brand" href="#top">hina<span>.</span></a>
			<div class="nav-links"><a href="#about">About</a><a href="#work">Work</a><a href="#contact">Contact</a></div>
			<a class="nav-cta" href="mailto:hello@hinatabbasum.com">Let's talk ↗</a>
		</nav>
	</header>

	<main id="top">
		<section class="hero wrap">
			<div class="hero-copy">
				<div class="eyebrow">Independent designer · Karachi / Worldwide</div>
				<h1>Making ideas feel <em>alive.</em></h1>
				<p>I’m Hina Tabbasum, a multidisciplinary designer turning thoughtful strategy into identities, digital experiences, and visual stories.</p>
				<a class="button" href="#work">Explore selected work <span class="arrow">↗</span></a>
			</div>
			<div class="hero-art">
				<img class="portrait" src="https://images.unsplash.com/photo-1551836022-d5d88e9218df?auto=format&fit=crop&w=900&q=85" alt="Creative team collaborating around a table">
				<div class="art-note">currently crafting<br>something good / 01</div>
			</div>
		</section>

		<div class="ticker"><div class="ticker-track">Brand identities <b>✳</b> Digital experiences <b>✳</b> Art direction <b>✳</b> Brand identities <b>✳</b> Digital experiences <b>✳</b> Art direction <b>✳</b></div></div>

		<section class="intro wrap" id="about">
			<div><div class="eyebrow">A little about me</div></div>
			<div class="intro-copy"><h2>Good design is a conversation between <em>clarity</em> and feeling.</h2><p>I work with curious people and ambitious teams to make their next chapter unmistakable. My process is collaborative, considered, and always grounded in the people you want to reach.</p><a class="text-link" href="mailto:hello@hinatabbasum.com">More about Hina ↗</a></div>
		</section>

		<section class="work" id="work">
			<div class="wrap">
				<div class="work-head"><div><div class="eyebrow">Selected projects / 2022—24</div><h2>A few things I’ve made.</h2></div><p>A small edit of identities and experiences made with good people.</p></div>
				<div class="projects">
					<a class="project" href="#contact"><div class="project-image"><img src="https://images.unsplash.com/photo-1497366754035-f200968a6e72?auto=format&fit=crop&w=1000&q=85" alt="Light-filled modern studio interior"></div><div class="project-info"><div><h3>Common Ground</h3><p>Brand identity · Strategy</p></div><span>↗</span></div></a>
					<a class="project" href="#contact"><div class="project-image"><img src="https://images.unsplash.com/photo-1558655146-d09347e92766?auto=format&fit=crop&w=1000&q=85" alt="Colorful design materials on a desk"></div><div class="project-info"><div><h3>Sunday Studio</h3><p>Digital experience · Art direction</p></div><span>↗</span></div></a>
					<a class="project" href="#contact"><div class="project-image"><img src="https://images.unsplash.com/photo-1545235617-9465d2a55698?auto=format&fit=crop&w=1000&q=85" alt="Editorial magazine and creative workspace"></div><div class="project-info"><div><h3>Field Notes</h3><p>Editorial · Campaign</p></div><span>↗</span></div></a>
				</div>
			</div>
		</section>

		<section class="contact wrap" id="contact"><div><div class="eyebrow">Have a project in mind?</div><h2>Let’s make it <em>real.</em></h2></div><div class="contact-main"><p>Whether you’re starting fresh or looking for a sharper point of view, I’d love to hear what you’re working on.</p><a class="email" href="mailto:hello@hinatabbasum.com">hello@hinatabbasum.com ↗</a></div></section>
	</main>
	<footer class="wrap"><span>© 2024 Hina Tabbasum</span><div class="socials"><a href="#top">Instagram</a><a href="#top">LinkedIn</a></div><span>Designed with intention</span></footer>
</body>
</html>
