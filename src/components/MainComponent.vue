<template>
	<div class="main__container">
		<main class="main__container--main">
			<section class="main__section--presentation">
				<h2>Låt mig presentera...</h2>
				<p>
					...mig själv! Joel del Pilar heter jag, 35år och front-end student på Medieinstitutet i stockholm. Jag söker LIA-plats till hösten 2023. Jag ser mycket fram emot att få komma ut och arbeta med alla de tekniker jag fått lära mig hittils och lära mig nytt. Jag hoppas kunna vara en som bidrar
					även som student.
				</p>
				<p>
					Jag vill bidra och lära mig mer om bl.a tillgänglighet (a11y), som är ett område jag finner intressant, hur kan vi skapa en bättre webb för alla? Att arbeta och bygga bra struktur i projekt, få bästa möjliga DX miljö, är något jag hoppas kunna lära mig mer om också. Självklart ska det bli
					spännande att lära mig mer om hur man arbetar i skarpa projekt, lära mig mer om JavaScript i ramverksmiljö.
				</p>
			</section>

			<section class="main__section--tell">
				<h2>Låt mig berätta...</h2>
				<p>...om utbildningen, vad jag kan och kommer ha kunskaper om när jag kommer ut på LIA. Innan LIA kommer vi läst all teori som utbildningen innehåller och därför kommer jag ha en bredd av kunskap inom bl.a :</p>
				<ul>
					<li class="html">HTML5</li>
					<li class="scss">CSS & SCSS</li>
					<li class="js">JavaScript & TypeScript</li>
					<li class="react">React</li>
					<li class="vue">Vue.js</li>
					<li class="api">API & node.js</li>
					<li class="test">Jest & Cypress</li>
					<li class="git">Versionshantering - GitHub</li>
					<li class="agil">Agilt arbete</li>
					<li class="figma">Figma</li>
				</ul>
			</section>
		</main>
		<aside class="main__container--aside">
			<div class="aside__img--container">
				<img
					src="../../public/joeldelpilar_profilepicture.webp"
					alt="smiling man with brown-red hair and beard, outside on the sidewalk."
					width="424"
					height="617"
				/>
			</div>

			<section class="aside__section">
				<h3>Snabb fakta</h3>
				<ul>
					<li>Modersmål: Svenska</li>
					<li>Engelska: Flytande tal & skrift</li>
					<li>Svenskt B-Körkort</li>
					<li>Vill gärna arbeta med JS-Ramverk</li>
					<li>Bekväm med TypeScript</li>
					<li>Intresserad av a11y - tillgänglighet</li>
				</ul>

				<p>I övrigt pratar jag gärna om klockor och analogfoto. Börjar vi prata musik och instrument så ligger gitarren mig varmt om hjärtat också.</p>
			</section>
		</aside>
	</div>
</template>

<script lang="ts">
	export default {
		data() {
			return {};
		},
	};
</script>

<style lang="scss" scoped>
	.main__container {
		width: 90vw;
		display: grid;
		grid-template-columns: 2fr 1fr;
		// background-color: hsla(0, 0%, 96%, 0.9);
		gap: 2rem;
		margin-inline: auto;
	}

	.main__container > * {
		background-color: hsla(0, 0%, 96%, 0.9);
		box-shadow: 0.5em 0.5rem 1rem hsla(0, 0%, 0%, 0.3);
	}

	.main__section--presentation,
	.main__section--tell {
		width: 90%;
		background-color: steelblue;
		margin-inline: auto;
		padding: 2rem;
		margin-block: 2rem;
		box-shadow: 0.5em 0.5rem 1rem hsla(0, 0%, 0%, 0.3);

		h2 {
			margin-inline: auto;
			font-size: 2rem;
			font-weight: 300;
			max-width: 70%;
		}

		p {
			margin-block-start: 1.5rem;
			margin-inline: auto;
			line-height: 1.5rem;
			max-width: 70%;
		}
	}

	.main__section--tell ul {
		margin-block-start: 1.5rem;
		margin-inline: auto;
		line-height: 1.5rem;
		max-width: 70%;
		list-style: inside;

		.html {
			list-style-image: url(./html.svg);
		}

		.scss {
			list-style-image: url(./css.svg);
		}

		.js {
			list-style-image: url(./js.svg);
		}

		.react {
			list-style-image: url(./react.svg);
		}

		.api {
			list-style-image: url(./api.svg);
		}

		.test {
			list-style-image: url(./testing.svg);
		}

		.agil {
			list-style-image: url(./agile.svg);
		}

		.vue {
			list-style-image: url(./vue.svg);
		}

		.git {
			list-style-image: url(./github.svg);
		}

		.figma {
			list-style-image: url(./figma.svg);
		}
	}

	.main__container--aside {
		position: relative;
		z-index: -2;

		.aside__img {
			position: relative;
		}
		.aside__img--container {
			position: relative;
			margin-block-start: 2rem;
			margin-inline: auto;
			clip-path: circle();
			background-color: #4682b4;

			img {
				width: 200px;
				height: auto;
				clip-path: circle();
				margin-inline: auto;
			}
		}

		.aside__section {
			display: flex;
			flex-direction: column;
			width: 90%;
			margin-block-start: 2rem;
			margin-inline: auto;
			justify-content: center;

			h3 {
				font-size: 2rem;
				font-weight: 300;
				text-align: center;
				word-spacing: 0.5rem;
				letter-spacing: 0.2rem;
				margin-block-end: 2rem;
			}

			ul {
				position: relative;
				margin-inline: auto;
				margin-block-end: 3rem;
				padding-block: 3rem;
				padding-inline: 5rem;
				// list-style: inside;
				list-style-image: url(../../public/arrowright.svg);
				li {
					line-height: 2rem;
				}
			}

			ul::after {
				content: '';
				position: absolute;
				z-index: -1;
				inset: 0;
				background-color: steelblue;
				box-shadow: 0.5em 0.5rem 1rem hsla(0, 0%, 0%, 0.3);
				transform: skewY(-1deg);
			}

			p {
				position: relative;
				max-width: 25rem;
				margin-inline: auto;
				padding: 2rem;
				margin-block-end: 2rem;
			}

			p::after {
				content: '';
				position: absolute;
				z-index: -1;
				inset: 0;
				background-color: steelblue;
				box-shadow: 0.5em 0.5rem 1rem hsla(0, 0%, 0%, 0.3);
				transform: skewY(-1deg);
			}
		}
	}

	@media (width <= 64em) {
		.main__container {
			display: flex;
			flex-direction: column;
		}

		.main__section--presentation {
			width: 95%;

			h2 {
				max-width: 95%;
			}

			p {
				max-width: 95%;
			}
		}
	}
</style>
