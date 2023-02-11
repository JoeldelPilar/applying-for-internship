<template>
	<footer class="footer__container">
		<section class="footer__container--grid">
			<div class="footer__grid--one">
				<ul>
					<li>
						<button
							type="button"
							title="mail to Joel"
							id="contactButton"
							@click="sendEmail"
						>
							Joel.delpilar@Medieinstitutet.se
						</button>
					</li>
					<li>location: <b>Stockholm, Sweden</b></li>
				</ul>
			</div>
			<div class="footer__grid--two">
				<a
					href="https://www.linkedin.com/in/joeldelpilar/"
					rel="noopener noreferrer"
					class="fa fa-linkedin fa_footer__custom"
					target="_blank"
					title="joel del pilar linkedin"
				></a>
			</div>
			<div class="footer__grid--three">
				<a
					href="https://github.com/JoeldelPilar"
					rel="noopener noreferrer"
					class="fa fa-github fa_footer__custom"
					target="_blank"
					title="joel del pilar github"
				></a>
			</div>
		</section>
	</footer>
</template>

<script lang="ts">
	export default {
		setup() {
			return {};
		},
		methods: {
			sendEmail() {
				window.location.href = 'mailto:joel.delpilar@medieinstitutet.se';
			},
		},
	};
</script>

<style lang="scss" scoped>
	.footer__container {
		position: relative;
		isolation: isolate;
		margin-block: 2rem;
		margin-inline: auto;
		width: 90vw;
		padding-block: 4rem;
		// background-color: hsla(0, 0%, 96%, 0.9);
		// box-shadow: 0.5em 0.5rem 1rem hsla(0, 0%, 0%, 0.3);
	}

	.footer__container::after {
		content: '';
		position: absolute;
		z-index: -1;
		inset: 0;
		background-color: hsla(0, 0%, 96%, 0.9);
		box-shadow: 0.5em 0.5rem 1rem hsla(0, 0%, 0%, 0.3);
		transform: skewY(-1deg);
	}

	.footer__container--grid {
		display: grid;
		grid-template-columns: 4fr 1fr 1fr;
		gap: 1rem;
		align-items: center;
		// justify-items: center;
		// background-color: hsla(0, 5%, 79%, 0.9);
	}

	.footer__grid--one {
		ul {
			margin-inline-start: 2rem;
			list-style: none;
			line-height: 2rem;
		}
	}
	.footer__grid--two {
		text-align: center;
		a {
			// width: 100%;
			font-size: 3rem;
			text-decoration: none;
			color: #0a66c2;
		}

		a:hover {
			opacity: 0.7;
			scale: 1.2;
		}
	}
	.footer__grid--three {
		text-align: left;
		a {
			// width: 100%;
			font-size: 3rem;
			text-decoration: none;
			color: #171515;
		}

		a:hover {
			opacity: 0.7;
			scale: 1.2;
		}
	}

	#contactButton {
		border: none;
		border-radius: 1rem;
		padding-inline: 0.5rem;
		cursor: pointer;
		background-color: hsla(207, 44%, 49%, 0.603);
	}

	#contactButton:hover {
		background-color: hsl(207, 44%, 49%);
	}

	@media screen and (min-width: 500px) {
		.footer__container--grid {
			grid-template-columns: 1fr 1fr;
			grid-template-rows: 2;
			justify-items: center;
		}

		.footer__grid--one {
			grid-column-start: 1;
			grid-column-end: 2;
			grid-row-start: 1;
			grid-row-end: 3;
			align-items: center;
		}

		.footer__grid--two {
			margin-block-end: 1rem;
		}

		.footer__grid--one {
			font-size: 0.9rem;

			ul {
				margin-inline-start: 1rem;
			}
		}
	}
</style>
