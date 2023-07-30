<template>
  <div class="menu-item">
		<div class="menu-item__icon">
			<img :src="itemIcon" alt="Icon">
		</div>
		<h3 class="menu-item__title">{{ title }}</h3>
  </div>
</template>

<script>

export default {
  name: 'MenuItem',
	props: {
		itemIcon: {
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