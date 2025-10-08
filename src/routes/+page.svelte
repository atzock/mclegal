
<script>
	const nav = [
		{ name: 'Start', href: '#' },
		{ name: 'Partner', href: '/partner' },
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
	h2 {
		color: #1a2233;
		font-size: 2.3rem;
		margin-top: 2.2rem;
		margin-bottom: 1.1rem;
		font-family: 'Lora', 'Playfair Display', 'Merriweather', serif;
		font-weight: 700;
		letter-spacing: 0.5px;
	}
	blockquote {
		font-style: italic;
		color: #444;
		border-left: 4px solid #e0b400;
		margin: 2.2rem 0 2.2rem 0;
		padding: 0.7rem 1.2rem;
		background: #fffbe6;
		border-radius: 8px;
		box-shadow: 0 2px 8px #e0b40011;
	}
	section {
		margin-bottom: 2.7rem;
	}

	button.btn-primary {
		font-family: 'Segoe UI', Arial, sans-serif;
		display: inline-flex;
		align-items: center;
		gap: 0.6rem;
		background: #e0b400;
		color: #fff;
		border: none;
		padding: 0.6rem 1rem;
		font-size: 1rem;
		font-weight: 700;
		border-radius: 12px;
		box-shadow: 0 6px 18px rgba(15,86,209,0.18), inset 0 -1px 0 rgba(255,255,255,0.06);
		cursor: pointer;
		transition: transform 0.12s ease, box-shadow 0.12s ease, opacity 0.12s ease;
		will-change: transform;
	}
	button.btn-primary svg {
		color: rgba(255,255,255,0.95);
		transform: translateX(0);
		transition: transform 0.18s ease;
	}
	button.btn-primary:hover {
		transform: translateY(-3px);
		box-shadow: 0 10px 26px rgba(15,86,209,0.22);
	}
	button.btn-primary:active {
		transform: translateY(-1px) scale(0.995);
	}
	button.btn-primary:focus {
		outline: 3px solid rgba(26,115,232,0.18);
		outline-offset: 3px;
	}
	@media (max-width: 700px) {
		button.btn-primary { font-size: 0.95rem; padding: 0.55rem 0.9rem; }
	}

	/* Small, subtle secondary button used inline */
	button.btn-secondary {
		font-family: 'Segoe UI', Arial, sans-serif;
		background: transparent;
		color: #1a2233;
		border: 1px solid rgba(26,34,51,0.08);
		padding: 0.18rem 0.36rem;
		font-size: 0.88rem;
		font-weight: 600;
		border-radius: 6px;
		line-height: 1;
		vertical-align: baseline;
		cursor: pointer;
		transition: background 0.14s ease, color 0.14s ease, transform 0.12s ease;
	}
	button.btn-secondary:hover {
		background: rgba(26,34,51,0.04);
		transform: translateY(-1px);
	}
	button.btn-secondary:active { transform: translateY(0); }
	button.btn-secondary:focus {
		outline: 2px solid rgba(224,180,0,0.18);
		outline-offset: 2px;
	}

	footer {
		background: #1a2233;
		color: #fff;
		text-align: center;
		padding: 1.2rem 0 1.2rem 0;
		border-top-left-radius: 24px;
		border-top-right-radius: 24px;
		margin-top: 3rem;
		font-size: 1.05rem;
		letter-spacing: 0.2px;
		box-shadow: 0 -2px 12px #0001;
		position: relative;
	}
	.footer-logo {
		max-width: 120px;
		margin: 0 auto 0.5rem auto;
		display: block;
		opacity: 0.85;
	}
		@media (max-width: 1200px) {
			.container {
				max-width: 98vw;
				padding: 1.2rem 1.2rem;
			}
		}
		@media (max-width: 900px) {
			.container {
				padding: 1.2rem 0.5rem;
			}
		}
		@media (max-width: 700px) {
			.container {
				padding: 0.7rem 0.2rem;
			}
			h2 {
				font-size: 1.3rem;
			}
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
	<blockquote>
		„Wer dem Recht zu dienen, aber nicht der Wahrheit dienen will, dem ist nicht zu trauen“<br />
		<span style="float:right; font-size:0.95em;">- John F. Kennedy</span>
	</blockquote>
	<h2>Ein Unternehmen stellt sich vor</h2>
	<p>
		“McLegal & Partner" ist die Anwaltskanzlei, der ihre Sorgen wichtiger sind als ihre Taten!<br>
		Gegründet 1922 von Mason McLee und nun in dritter Hand geführt, beweist McLegal stetig ihre Fachkompetenz und erweitert ihr Spektrum an engagierten Rechtsanwälten seit jeher.<br>
		Im Jahr 2025 möchten wir den großen Schritt wagen und in großem Ausmaß expandieren. Zusammen mit Tino de Vries und Hannes Davis, die ihren Weg zum Juristen erst vor Kurzem durch das Bestehen des “Bar Exam” und den Bachelor an der YLS, Connecticut gefunden haben, sucht sich McLegal nun größere Aufgaben innerhalb der Vereinigten Staaten.
	</p>
	<section id="partner" style="margin-top:3rem;">
		<h2>Unsere Senior & Junior Partner</h2>
		<button class="btn-primary" on:click={() => window.location.href = '/partner'} aria-label="Mehr über unsere Partner">
			<span>Siehe mehr</span>
			<svg aria-hidden="true" focusable="false" width="16" height="16" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
				<path d="M5 12h14M13 5l6 7-6 7" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
			</svg>
		</button>
	</section>
	<section id="leitbild" style="margin-top:3rem;">
		<h2>Unser Leitbild</h2>
		<p>
			Ihr Verfahren ist unser Vorhaben! Nach einem starken Jahr 2024 wird McLegal & Partner auch 2025 wieder mit einem Unternehmenswachstum und einem finanziellen Gleichgewicht belohnt werden.<br>
			Wir setzen auf Kompetenz, Sachlichkeit und Reife, damit wir Ihnen in den schwierigsten Zeiten sowohl emotional als auch faktisch eine Hand reichen können!
		</p>
	</section>
	<section id="kanzlei" style="margin-top:3rem;">
		<h2>Unsere Kanzlei</h2>
		<p>
			Der Brennpunkt für Ihren Anspruch an die Judikative befindet sich in perfekter Lage in West Vinewood!<br>
			Wir legen viel Wert auf gute Anbindung an den lokalen ÖPNV und eine gute Erreichbarkeit, auch für Staatsdiener.<br>
			Einen Einblick in unsere Niederlassung finden Sie 
			<button class="btn-secondary" on:click={() => window.open('https://youtu.be/rHn0pKgGuDU?si=p8qdF_z3Up6CkYpL', '_blank')} style="margin-left:0.4em;">
				hier
			</button>.
		</p>
	</section>
</main>

<footer>
	<img src="/mclegal-logo-white.png" alt="McLegal Logo" class="footer-logo" />
	&copy; 2025 McLegal & Partner – Legal ist McLegal
</footer>
