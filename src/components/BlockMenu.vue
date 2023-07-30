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

import {
	dashboard,
	invoice,
	files,
	events,
	teams,
	massage,
	settings,
}
from '@/assets/js/iconsMenu'

export default {
  name: 'BlockMenu',
  components: {
    MenuItem,
  },
	data() {
		return {
			dashboard: dashboard,
			invoice: invoice,
			files: files,
			events: events,
			teams: teams,
			massage: massage,
			settings: settings,
		}
	}
}
</script>