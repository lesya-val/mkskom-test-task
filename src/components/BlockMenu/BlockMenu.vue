<template>
  <div :class="$style['block-menu']">
    <div :class="$style['block-menu__line']">
      <MenuItem :icon="dashboard" title="Dashboard" />
      <MenuItem :icon="dashboard" title="Notes" />
    </div>
    <div :class="$style['block-menu__line']">
      <MenuItem :icon="invoice" title="Invoice" />
      <MenuItem :icon="files" title="Files" />
    </div>
    <div :class="$style['block-menu__line']">
      <MenuItem :icon="events" title="Events" />
      <MenuItem :icon="teams" title="Teams" />
    </div>
    <div :class="$style['block-menu__line']">
      <MenuItem :icon="massage" title="Massage" />
      <MenuItem :icon="settings" title="Settings" />
    </div>
  </div>
</template>

<script>

import MenuItem from '@/components/MenuItem/MenuItem.vue'
import { dashboard, invoice, files, events, teams, massage, settings, } from '@/assets/js/icons'
import styles from '@/components/BlockMenu/BlockMenu.module.scss'

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
	},
	computed: {
    $style() {
      return styles;
    },
  },
}

</script>