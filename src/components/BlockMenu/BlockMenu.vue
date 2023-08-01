<template>
  <div :class="$style['block-menu']">
    <div v-for="(menuItem, index) in menuItems" :key="index" :class="$style['block-menu__line']">
      <MenuItem 
				:icon="menuItem.icon" 
				:title="menuItem.title"
				:isActive="index === activeItemIndex"
				@click="handleMenuItem(index)"
			/>
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

			menuItems: [
				{ icon: dashboard, title: 'Dashboard' },
				{ icon: dashboard, title: 'Notes' },
				{ icon: invoice, title: 'Invoice' },
				{ icon: files, title: 'Files' },
				{ icon: events, title: 'Events' },
				{ icon: teams, title: 'Teams' },
				{ icon: massage, title: 'Massage' },
				{ icon: settings, title: 'Settings' },
			],
			activeItemIndex: null,
		}
	},
	methods: {
		handleMenuItem(index) {
			this.activeItemIndex = index
		}
	},
	computed: {
    $style() {
      return styles;
    },
  },
}

</script>