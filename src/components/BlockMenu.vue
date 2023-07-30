<template>
  <div class="block-menu">
		<div class="block-menu__line">
			<MenuItem
				:itemIcon="dashboard"
				title="Dashboard"
			/>
			<MenuItem
				:itemIcon="dashboard"
				title="Notes"
			/>
		</div>
		<div class="block-menu__line">
			<MenuItem
				:itemIcon="invoice"
				title="Invoice"
			/>
			<MenuItem
				:itemIcon="files"
				title="Files"
			/>
		</div>
		<div class="block-menu__line">
			<MenuItem
				:itemIcon="events"
				title="Events"
			/>
			<MenuItem
				:itemIcon="teams"
				title="Teams"
			/>
		</div>
		<div class="block-menu__line">
			<MenuItem
				:itemIcon="massage"
				title="Massage"
			/>
			<MenuItem
				:itemIcon="settings"
				title="Settings"
			/>
		</div>
  </div>
</template>

<script>

import MenuItem from '@/components/MenuItem.vue'

export default {
  name: 'BlockMenu',
  components: {
    MenuItem,
  },
	data() {
		return {
			dashboard: require('../assets/image/iconsMenu/dashboard.svg'),
			invoice: require('../assets/image/iconsMenu/invoice.svg'),
			files: require('../assets/image/iconsMenu/files.svg'),
			events: require('../assets/image/iconsMenu/events.svg'),
			teams: require('../assets/image/iconsMenu/teams.svg'),
			massage: require('../assets/image/iconsMenu/massage.svg'),
			settings: require('../assets/image/iconsMenu/settings.svg'),
		}
	}
}
</script>