<template>
  <div class="navigation">
    <NavigationContent/>
  </div>
</template>

<script>

import NavigationContent from '@/components/NavigationContent.vue'

export default {
  name: "NavigationBar",
  components: {
    NavigationContent,
  }
};

</script>

<style lang="scss">
  .navigation {
		border-bottom: solid 2px var(--gray-blue-grey-blue-95, #edeff2);
	}
</style>