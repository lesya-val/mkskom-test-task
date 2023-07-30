<template>
  <div class="sidebar-gallery">
		<div class="sidebar-gallery__folders">
			<ButtonWithIcon
			class="sidebar-gallery__btn"
			:icon="note"
			name="New Note"
			/>
			<div class="sidebar-gallery__menu">
				<IconAndTitle
					class="sidebar-gallery__all"
					:icon="folder"
					title="All Notes"
					number=43
				/>
				<div class="sidebar-gallery__list">
					<IconAndTitle
						:icon="folder"
						title="Design"
						number=23
					/>
					<IconAndTitle
						:icon="folder"
						title="Code Blocks"
						number=15
					/>
					<IconAndTitle
						:icon="folder"
						title="Drafts"
						number=18
					/>
					<IconAndTitle
						:icon="folder"
						title="Peoples Review"
						number=21
					/>
					<IconAndTitle
						:icon="folder"
						title="Social"
						number=43
					/>
					<IconAndTitle
						:icon="folder"
						title="Labels"
						number=36
					/>
					<IconAndTitle
						:icon="folder"
						title="My Notes"
						number=29
					/>
				</div>
				<IconAndTitle
					class="sidebar-gallery__add"
					:icon="plus"
					title="Add Folter"
				/>
			</div>
		</div>
		<div class="sidebar-gallery__labels">
			<h3>Labels</h3>
			<div class="sidebar-gallery__list">
				<IconAndTitle
				class="sidebar-gallery__label"
				:icon="label"
				title="Notes"
				/>
				<IconAndTitle
					class="sidebar-gallery__label"
					:icon="label"
					title="Change Notes"
				/>
				<IconAndTitle
					class="sidebar-gallery__label"
					:icon="label"
					title="From Family"
				/>
				<IconAndTitle
					class="sidebar-gallery__label"
					:icon="label"
					title="Imagium"
				/>
				<IconAndTitle
					class="sidebar-gallery__label"
					:icon="label"
					title="Work"
				/>
				<IconAndTitle
					class="sidebar-gallery__label"
					:icon="plus"
					title="New Label"
				/>
			</div>
		</div>
	</div>

</template>

<script>

import ButtonWithIcon from '@/components/ButtonWithIcon.vue'
import IconAndTitle from '@/components/IconAndTitle.vue'

import {
	note,
	folder,
	plus,
	label,
}
from '@/assets/js/icons.js'

export default {
  name: "SidebarGallery",
  components: {
    ButtonWithIcon,
		IconAndTitle,
	},
	data() {
		return {
			note: note,
			folder: folder,
			plus: plus,
			label: label,
		}
	}
};

</script>