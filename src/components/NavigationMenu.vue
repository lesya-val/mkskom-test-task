<template>
	<nav class="navigation__menu">
		<ul class="navigation__list">
			<li class="navigation__item">Dashboard</li>
			<li class="navigation__item">About Us</li>
			<li class="navigation__item">News</li>
			<li class="navigation__item">User Policy</li>
			<li class="navigation__item">Contacts</li>
		</ul>
		<button class="navigation__ellipsis-menu" type="button">
					<svg
						width="31"
						height="30"
						viewBox="0 0 31 30"
						fill="none"
						xmlns="http://www.w3.org/2000/svg"
						>
						<path
							fill-rule="evenodd"
							clip-rule="evenodd"
							d="M9.33337 13C8.23337 13 7.33337 13.9 7.33337 15C7.33337 16.1 8.23337 17 9.33337 17C10.4334 17 11.3334 16.1 11.3334 15C11.3334 13.9 10.4334 13 9.33337 13ZM21.3334 13C20.2334 13 19.3334 13.9 19.3334 15C19.3334 16.1 20.2334 17 21.3334 17C22.4334 17 23.3334 16.1 23.3334 15C23.3334 13.9 22.4334 13 21.3334 13ZM15.3334 13C14.2334 13 13.3334 13.9 13.3334 15C13.3334 16.1 14.2334 17 15.3334 17C16.4334 17 17.3334 16.1 17.3334 15C17.3334 13.9 16.4334 13 15.3334 13Z"
							fill="#C3CAD9"
						/>
					</svg>
		</button>
	</nav>
</template>

<script>

export default {
	name: "NavigationMenu",
};

</script>

<style lang="scss">
	.navigation {
		&__menu {
			display: flex;
			justify-content: center;
			align-items: center;
			column-gap: 25px;
		}

		&__list {
			display: flex;
			justify-content: center;
			align-items: center;
			column-gap: 25px;

			color: var(--gray-blue-grey-blue-70, #7d8fb3);
			font: var(--bold-bold-13, 700 13px/25px "Roboto", sans-serif);
		}
	}
</style>