<template>
	<div class="hero__container">
		<section class="hero__container--heading">
			<h1>LIA Hösten 2023</h1>
			<p>Stockholm 23 Oktober - 29 December</p>
		</section>
		<HamburgerMenu class="hero__container__menu--btn" />
	</div>
</template>

<script lang="ts">
	import HamburgerMenu from '../components/parts/HamburgerMenu.vue';
	export default {
		components: {
			HamburgerMenu,
		},
	};
</script>

<style lang="scss">
	.hero__container {
		width: 90vw;
		margin-block: 2rem;
		padding: 2rem;
		display: flex;
		margin-inline: auto;
		justify-content: center;
		align-items: center;
		background-color: hsla(0, 0%, 96%, 0.9);
		box-shadow: 0.5em 0.5rem 1rem hsla(0, 0%, 0%, 0.3);
	}

	.hero__container--heading {
		flex-basis: 100%;
		text-align: center;

		h1 {
			font-size: 3rem;
			font-weight: 300;
			letter-spacing: 0.5rem;
		}
	}

	@media screen and (min-width: 1024px) {
		.hero__container--heading {
			h1 {
				font-size: 1.5rem;
			}
		}
	}
</style>
