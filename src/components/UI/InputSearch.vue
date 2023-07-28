<template>
	<div class="input-search">
		<button>
			<svg
			class="icon"
			width="24"
			height="24"
			viewBox="0 0 24 24"
			fill="none"
			xmlns="http://www.w3.org/2000/svg"
		>
			<path
				fill-rule="evenodd"
				clip-rule="evenodd"
				d="M14.8005 13.6005H14.1685L13.9445 13.3845C14.9045 12.2645 15.4005 10.7365 15.1285 9.11249C14.7525 6.88849 12.8965 5.11249 10.6565 4.84049C7.27255 4.42449 4.42455 7.27249 4.84055 10.6565C5.11255 12.8965 6.88855 14.7525 9.11255 15.1285C10.7365 15.4005 12.2645 14.9045 13.3845 13.9445L13.6005 14.1685V14.8005L17.0005 18.2005C17.3285 18.5285 17.8645 18.5285 18.1925 18.2005C18.5205 17.8725 18.5205 17.3365 18.1925 17.0085L14.8005 13.6005ZM10.0005 13.6005C8.00855 13.6005 6.40055 11.9925 6.40055 10.0005C6.40055 8.00849 8.00855 6.40049 10.0005 6.40049C11.9925 6.40049 13.6005 8.00849 13.6005 10.0005C13.6005 11.9925 11.9925 13.6005 10.0005 13.6005Z"
				fill="#C3CAD9"
			/>
			</svg>
		</button>
    <input class="input-search__input" type="text" placeholder="Search">
	</div>
</template>

<script>

export default {
	name: "InputSearch",
};

</script>

<style lang="scss">
	.input-search {
		display: flex;
		background: var(--white-white, #ffffff);
		border-radius: 30px ;
		border: 2px solid var(--gray-blue-grey-blue-97, #f5f6f7);
		padding: 15px;
		gap: 10px;
		align-items: center;
		width: 180px;
		height: 40px;
		box-shadow: var(
		--shadows-gray-blue-30-3-5-b-box-shadow,
		0px 2px 5px 0px rgba(38, 51, 77, 0.03));

		&__input {
			max-width: 116px;
		}

		&__input::placeholder {
			color: var(--gray-blue-grey-blue-70, #7d8fb3);
			font: var(--black-black-10, 900 10px/20px "Roboto", sans-serif);
		}
}
</style>