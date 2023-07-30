<template>
  <div class="menu-item">
		<div class="menu-item__icon">
			<span
				v-html="icon" class="icon">
			</span>
		</div>
		<h3 class="menu-item__title">{{ title }}</h3>
  </div>
</template>

<script>

export default {
  name: 'MenuItem',
	props: {
		icon: {
      type: String,
      required: true,
    },
		title: {
			type: String,
			required: true,
		},
	}
}
</script>