---
layout: default
title: "Inicio"
permalink: /
---
<!-- test reference: https://www.enonic.com/ -->
<section class="hero-section">
	<div class="hero-container">
		<div class="hero-content home">
			<div class="home-hero-text-cta">
				<h1>Cómo Podemos Ayudarte:</h1>
				<p class="hero-description">Innovación digital para tu empresa: Desarrollo web y software, ciberseguridad, diseño impactante, marketing digital, IoT, IA y consultoría estratégica. <br>Todo lo que necesitas para crecer y destacarte.
				</p>
				<div class="hero-button-wrapper">
					<a href="#" class="hero-button">Contáctanos</a>
				</div>
			</div>
			<div class="home-hero-screenshot">
				<svg role="img" viewBox="0 0 366 729" class="fy up wb bhx">
					<title>App screenshot</title>
					<defs>
						<clipPath id="clip">
							<rect rx="36" width="316" height="684" />
						</clipPath>
					</defs>
					<path d="M363.315 64.213C363.315 22.99 341.312 1 300.092 1H66.751C25.53 1 3.528 22.99 3.528 64.213v44.68l-.857.143A2 2 0 0 0 1 111.009v24.611a2 2 0 0 0 1.671 1.973l.95.158a2.26 2.26 0 0 1-.093.236v26.173c.212.1.398.296.541.643l-1.398.233A2 2 0 0 0 1 167.009v47.611a2 2 0 0 0 1.671 1.973l1.368.228c-.139.319-.314.533-.511.653v16.637c.221.104.414.313.56.689l-1.417.236A2 2 0 0 0 1 237.009v47.611a2 2 0 0 0 1.671 1.973l1.347.225c-.135.294-.302.493-.49.607v377.681c0 41.213 22 63.208 63.223 63.208h95.074c.947-.504 2.717-.843 4.745-.843l.141.001h.194l.086-.001 33.704.005c1.849.043 3.442.37 4.323.838h95.074c41.222 0 63.223-21.999 63.223-63.212v-394.63c-.259-.275-.48-.796-.63-1.47l-.011-.133 1.655-.276A2 2 0 0 0 366 266.62v-77.611a2 2 0 0 0-1.671-1.973l-1.712-.285c.148-.839.396-1.491.698-1.811V64.213Z" fill="#4B5563" />
					<path d="M16 59c0-23.748 19.252-43 43-43h246c23.748 0 43 19.252 43 43v615c0 23.196-18.804 42-42 42H58c-23.196 0-42-18.804-42-42V59Z" fill="#343E4E" />
					<!-- Group all images and apply the clipPath -->
					<g clip-path="url(#clip)" transform="translate(24 24)">
						<image class="slide slide1" href="assets/img/novapay.png" width="316" height="684" preserveAspectRatio="xMidYMid slice" />
						<image class="slide slide2" href="assets/img/novapay2.png" width="316" height="684" preserveAspectRatio="xMidYMid slice" />
						<image class="slide slide3" href="assets/img/novapay3.png" width="316" height="684" preserveAspectRatio="xMidYMid slice" />
					</g>
				</svg>
			</div>
		</div>
	</div>
</section>
<section class="services">
	<div class="services__container">
		<h2>Nuestros Servicios:</h2> 
		<ul class="services__list">
			{% assign servicios_values = site.data.servicios | values %}
			{% for pair in servicios_values %}
			{% assign servicio = pair[1] %}
			<li class="services__item">
				<a class="services__link" href="{{ servicio.hero.permalink }}">
					<div class="services__icon">
						<img src="{{ servicio.hero.icon | relative_url}}">
					</div>
					<h2 class="services__title">{{ servicio.hero.title }}</h2>
					<p class="services__description">{{ servicio.hero.tagline }}</p>
				</a>
			</li>
			{% endfor %}
		</ul>
	</div>
</section>
<section id="beneficios">
	<div class="beneficios__container">
		<h2>Por qué elegirnos:</h2>
		<p class="desc">Elige nuestras soluciones personalizadas y obtén el máximo potencial para tu negocio. Contamos con un equipo experto en desarrollo, IA y marketing digital, enfocados en ofrecerte resultados medibles que impulsan tu crecimiento y rentabilidad. 🚀</p>
		<ul class="grid">
			<li class="icon-personalized">
				<strong>Atención personalizada</strong>
				<p>Desarrollamos soluciones a medida, ofreciendo un servicio cercano y adaptado a las necesidades específicas de cada cliente.</p>
			</li>
			<li class="icon-experience">
				<strong>Experiencia comprobada</strong>
				<p>Contamos con un equipo de profesionales con amplia trayectoria, garantizando calidad y eficiencia en cada proyecto.</p>
			</li>
			<li class="icon-innovation">
				<strong>Innovación constante</strong>
				<p>Aplicamos tecnologías de vanguardia y enfoques creativos que posicionan a nuestros clientes a la delantera en el mercado.</p>
			</li>
			<li class="icon-measurable">
				<strong>Resultados medibles:</strong>
				<p>Estrategias respaldadas por métricas y análisis que aseguran un retorno positivo de inversión.</p>
			</li>
		</ul>
	</div>
</section>
<section id="casos">
	<h2>Casos de Éxito</h2>
	<p><strong>SEO para E-commerce:</strong> Aumento de tráfico en un 200% en 3 meses.</p>
	<p><strong>Automatización con IA:</strong> Reducción de costos operativos en un 50% con procesos optimizados.</p>
	<p><strong>Desarrollo de Marketplace:</strong> Incremento de ventas online en un 300% tras el lanzamiento.</p>
</section>
<section id="testimonios">
	<h2>Lo Que Dicen Nuestros Clientes</h2>
	<blockquote>"Desde que implementamos sus estrategias, nuestro negocio ha crecido de manera exponencial en el mercado digital." - CEO de Startup</blockquote>
	<blockquote>"Nos ayudaron a optimizar nuestra seguridad digital y ahora operamos con total tranquilidad." - Director de IT</blockquote>
</section>
<section id="blog">
	<h2>Recursos Exclusivos</h2>
	<p>Mantente al día con las últimas tendencias en tecnología, inteligencia artificial y estrategias digitales.</p>
	<a href="#">Accede a Nuestros Artículos</a>
</section>
<section id="contacto">
	<h2>¡Hablemos de tu Proyecto!</h2>
	<p>Agenda una consulta gratuita y descubre cómo podemos llevar tu negocio al siguiente nivel.</p>
	<form>
		<label for="nombre">Nombre:</label>
		<input type="text" id="nombre" name="nombre" required>
		<br>
		<label for="email">Email:</label>
		<input type="email" id="email" name="email" required>
		<br>
		<label for="mensaje">Mensaje:</label>
		<textarea id="mensaje" name="mensaje" required></textarea>
		<br>
		<button type="submit"><strong>Solicitar Consulta</strong></button>
	</form>
</section>
