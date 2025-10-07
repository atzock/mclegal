<script>
	const nav = [
		{ name: 'Start', href: '#' },
		{ name: 'Partner', href: '#partner' },
		{ name: 'Kanzlei', href: '#kanzlei' },
		{ name: 'Leitbild', href: '#leitbild' }
	];
	let active = 'Start';
</script>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Lora:wght@700&family=Playfair+Display:wght@700&display=swap');

	:global(body) {
		font-family: 'Segoe UI', Arial, sans-serif;
		background: linear-gradient(135deg, #f7f7f9 60%, #fffbe6 100%);
		margin: 0;
		color: #222;
		min-height: 100vh;
	}
	header {
		background: linear-gradient(90deg, #1a2233 60%, #e0b400 100%);
		color: #fff;
		padding: 2.5rem 0 1.5rem 0;
		text-align: center;
		box-shadow: 0 2px 16px #0002;
		position: relative;
		border-bottom-left-radius: 32px;
		border-bottom-right-radius: 32px;
		overflow: hidden;
	}
	.header-logo {
		max-width: 260px;
		display: block;
		margin: 0 auto 0.5rem auto;
		filter: drop-shadow(0 2px 8px #0003);
	}
	.container {
		max-width: 1240px;
		margin: 2.5rem auto 2rem auto;
		background: #fff;
		border-radius: 20px;
		box-shadow: 0 6px 32px #0001, 0 1.5px 0 #e0b40011;
		padding: 2.7rem 3.2rem 2.2rem 3.2rem;
		position: relative;
		z-index: 1;
	}
	nav {
		margin: 1.2rem 0 0.5rem 0;
		display: flex;
		justify-content: center;
		gap: 0.5rem;
		flex-wrap: wrap;
	}
	nav a {
		color: #fff;
		text-decoration: none;
		margin: 0 0.7rem;
		font-weight: 600;
		letter-spacing: 0.5px;
		transition: color 0.2s, background 0.2s, border-radius 0.2s;
		border-bottom: 2.5px solid transparent;
		padding: 0.3rem 1.1rem 0.3rem 1.1rem;
		border-radius: 18px 18px 0 0;
		font-size: 1.08rem;
		position: relative;
	}

	h1 {
		font-size: 2.9rem;
		margin-bottom: 0.5rem;
		letter-spacing: 1px;
		font-family: 'Playfair Display', 'Lora', 'Merriweather', serif;
		font-weight: 700;
		color: #1a2233;
	}
	h2 {
		color: #1a2233;
		font-size: 2.3rem;
		margin-top: 2.2rem;
		margin-bottom: 1.1rem;
		font-family: 'Lora', 'Playfair Display', 'Merriweather', serif;
		font-weight: 700;
		letter-spacing: 0.5px;
	}
	h3 {
		font-size: 1.22rem;
		margin-bottom: 0.3rem;
		font-family: 'Lora', 'Playfair Display', 'Merriweather', serif;
		font-weight: 700;
		color: #1a2233;
	}
	section {
		margin-bottom: 2.7rem;
	}
	.partner-cards {
		display: flex;
		flex-wrap: wrap;
		gap: 2.2rem;
		margin-top: 1.7rem;
		justify-content: center;
	}
	.partner-card {
		flex: 1 1 420px;
		background: linear-gradient(120deg, #f7f7f9 80%, #fffbe6 100%);
		border-radius: 22px;
		padding: 2.7rem 2.2rem 2.2rem 2.2rem;
		box-shadow: 0 4px 24px #e0b40011, 0 2px 0 #e0b40008;
		min-width: 340px;
		max-width: 480px;
		margin-bottom: 1.2rem;
		border: 2px solid #e0b40022;
		transition: transform 0.15s, box-shadow 0.15s;
		position: relative;
		display: flex;
		flex-direction: column;
		align-items: center;
		overflow: hidden;
	}
	.partner-card:hover {
		transform: translateY(-4px) scale(1.025);
		box-shadow: 0 8px 32px #e0b40022, 0 2px 0 #e0b40011;
		z-index: 2;
	}
	.partner-card .role {
		font-weight: 700;
		color: #e0b400;
		margin-bottom: 0.2rem;
		font-size: 1.05rem;
	}
	.partner-card .logo-bg {
		width: 38px;
		height: 38px;
		position: absolute;
		top: 1.1rem;
		right: 1.1rem;
		opacity: 0.13;
		pointer-events: none;
	}
	.partner-img {
		width: 92px;
		height: 92px;
		object-fit: cover;
		border-radius: 50%;
		border: 2.5px solid #e0b40044;
		margin-bottom: 1.1rem;
		background: #fffbe6;
		box-shadow: 0 2px 8px #e0b40011;
		z-index: 1;
	}
	.partner-card .logo-bg {
		z-index: 0;
	}
</style>

<header>
  <img src="/mclegal-logo-white.png" alt="McLegal & Partner Logo" class="header-logo" />
  <nav>
    {#each nav as item}
      <a href={item.href} class:item-active={active === item.name} on:click={() => active = item.name}>{item.name}</a>
    {/each}
  </nav>
</header>
<main class="container">
	<section id="partner" style="margin-top:3rem;">
		<h2>Unsere Senior & Junior Partner</h2>
		<div class="partner-cards">
					<div class="partner-card">
						<img src="/mclegal-logo.png" alt="Logo" class="logo-bg" />
						<img src="/matze-mclee.jpg" alt="Matze McLee" class="partner-img" on:error={(e) => e.target.style.display = 'none'} />
						<h3 style="margin-top:0; color:#1a2233;">Matze McLee</h3>
						<div class="role">Senior Partner</div>
						<div>Fachanwalt für Strafrecht, Zivilrecht, Medienrecht</div>
						<div style="margin:1.1rem 0 0.5rem 0; color:#444; font-size:1.07rem; text-align:center;">
							<strong>Vita:</strong> Studium an der Universität Köln, seit 2001 bei McLegal, spezialisiert auf komplexe Strafprozesse und Medienrecht.
						</div>
						<div style="color:#888; font-size:0.98rem; margin-bottom:0.7rem; text-align:center;">
							<em>"Recht haben ist gut. Aber Recht bekommen ist besser."</em>
						</div>
						<div style="font-size:0.98rem; color:#1a2233; margin-bottom:0.2rem;">
							<strong>Kontakt:</strong> matze.mclee@mclegal.com
						</div>
					</div>
					<div class="partner-card">
						<img src="/mclegal-logo.png" alt="Logo" class="logo-bg" />
						<img src="/tino-devries.jpg" alt="Tino de Vries" class="partner-img" on:error={(e) => e.target.style.display = 'none'} />
						<h3 style="margin-top:0; color:#1a2233;">Tino de Vries</h3>
						<div class="role">Junior Partner</div>
						<div>Fachanwalt für Strafrecht, Arzthaftungsrecht</div>
						<div style="margin:1.1rem 0 0.5rem 0; color:#444; font-size:1.07rem; text-align:center;">
							<strong>Vita:</strong> Yale Law School, Berufseinstieg 2023, engagiert für Patientenrechte und medizinische Ethik.
						</div>
						<div style="color:#888; font-size:0.98rem; margin-bottom:0.7rem; text-align:center;">
							<em>"Ich bin ein Anwalt. Und selbst Drogenhändler brauchen Anwälte."</em>
						</div>
						<div style="font-size:0.98rem; color:#1a2233; margin-bottom:0.2rem;">
							<strong>Kontakt:</strong> tino.devries@mclegal.com
						</div>
					</div>
					<div class="partner-card">
						<img src="/mclegal-logo.png" alt="Logo" class="logo-bg" />
						<img src="/hannes-davis.jpg" alt="Hannes Davis" class="partner-img" on:error={(e) => e.target.style.display = 'none'} />
						<h3 style="margin-top:0; color:#1a2233;">Hannes Davis</h3>
						<div class="role">Junior Partner</div>
						<div>Fachanwalt für Verkehrsrecht, Staatsrecht, Beamtenrecht</div>
						<div style="margin:1.1rem 0 0.5rem 0; color:#444; font-size:1.07rem; text-align:center;">
							<strong>Vita:</strong> Bachelor an der YLS, Connecticut, seit 2024 bei McLegal, Experte für öffentliches Dienstrecht.
						</div>
						<div style="color:#888; font-size:0.98rem; margin-bottom:0.7rem; text-align:center;">
							<em>"Das Recht ist für die Menschen da."</em>
						</div>
						<div style="font-size:0.98rem; color:#1a2233; margin-bottom:0.2rem;">
							<strong>Kontakt:</strong> hannes.davis@mclegal.com
						</div>
					</div>
					<div style="width:100%;display:flex;justify-content:center;margin-top:2.2rem;">
						<button
							style="background:#1a2233;color:#fff;font-weight:700;font-size:1.13rem;padding:0.8rem 2.5rem;border:none;border-radius:18px;cursor:pointer;box-shadow:0 2px 12px #0001;transition:background 0.15s, color 0.15s;letter-spacing:0.5px;"
							on:click={() => window.location.href = '/'}
							on:mouseover={(e) => {e.target.style.background='#e0b400';e.target.style.color='#1a2233';}}
							on:mouseout={(e) => {e.target.style.background='#1a2233';e.target.style.color='#fff';}}
						>
							Zurück zur Hauptseite
						</button>
					</div>
		</div>
	</section>
</main>