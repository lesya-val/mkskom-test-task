<template>
  <div class="block-menu">
		<div class="block-menu__line">
			<MenuItem
				:icon="dashboard"
				title="Dashboard"
			/>
			<MenuItem
				:icon="dashboard"
				title="Notes"
			/>
		</div>
		<div class="block-menu__line">
			<MenuItem
				:icon="invoice"
				title="Invoice"
			/>
			<MenuItem
				:icon="files"
				title="Files"
			/>
		</div>
		<div class="block-menu__line">
			<MenuItem
				:icon="events"
				title="Events"
			/>
			<MenuItem
				:icon="teams"
				title="Teams"
			/>
		</div>
		<div class="block-menu__line">
			<MenuItem
				:icon="massage"
				title="Massage"
			/>
			<MenuItem
				:icon="settings"
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
from '@/assets/js/icons'

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