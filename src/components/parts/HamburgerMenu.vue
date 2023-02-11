<template>
	<button
		class="material-symbols-outlined menu__btn"
		@click="toggleMenu"
		id="ham-menu"
	>
		menu
	</button>
	<transition>
		<nav
			v-if="toggleMenuState"
			class="menu__container"
		>
			<ul class="menu__list">
				<li class="menu__list--item">
					<a
						href="./CV_JoelDelPilar.pdf"
						download="Joel Del Pilar CV"
						rel="noopener noreferrer"
						target="_blank"
						>CV
					</a>
				</li>
				<li class="menu__list--item">
					<a
						href="https://www.linkedin.com/in/joeldelpilar/"
						rel="noopener noreferrer"
						target="_blank"
						>Linkedin
					</a>
				</li>
				<li class="menu__list--item">
					<a
						href="https://github.com/JoeldelPilar"
						rel="noopener noreferrer"
						target="_blank"
						>GitHub
					</a>
				</li>
			</ul>
		</nav>
	</transition>
</template>

<script lang="ts">
	import { Transition } from 'vue';

	export default {
		data() {
			props: {
			}
			return {
				toggleMenuState: false,
			};
		},
		methods: {
			toggleMenu() {
				this.toggleMenuState = !this.toggleMenuState;
				let state = document.getElementById('ham-menu') as HTMLButtonElement;
				if (this.toggleMenuState === false) {
					state.innerHTML = 'menu';
				} else {
					state.innerHTML = 'close';
				}
			},
		},
	};
</script>

<style lang="scss" scoped>
	.menu__btn {
		border: 0;
		width: 2.8125rem;
		height: 2.8125rem;
		scale: 1.25;
		z-index: 50;
	}

	.menu__container {
		position: absolute;
		top: 0;
		margin-inline: auto;
		width: 90vw;
		text-align: center;
		padding: 10rem;
		margin-block-start: 12rem;
		background-color: hsla(220, 11%, 84%, 0.9);
	}

	.menu__list {
		list-style: none;
		display: flex;
		flex-direction: column;
		gap: 2.5rem;
		.menu__list--item a {
			text-decoration: none;
			font-size: 2rem;
			font-weight: 400;
			color: black;
		}
	}

	.v-enter-active,
	.v-leave-active {
		transition: opacity 0.3s ease;
	}

	.v-enter-from,
	.v-leave-to {
		opacity: 0;
	}

	@media (min-width: 1024px) {
		.menu__container {
			margin-block-start: 2rem;
			padding-inline: 6rem;
			background-color: hsla(220, 11%, 84%, 0.95);
		}
	}
</style>
