<template>
  <div class="tabs d-flex align-items-center mx-auto">
    <div 
      v-for="(mode, index) in modes" 
      :key="index"
      :class="[colorMode === mode ? 'active' : 'inactive', 'tab']"
      @click="$colorMode.preference = mode"
    >
      <div :class="[index === 0 ? 'left' : 'right', colorMode === mode ? 'active' : 'inactive', 'background-tab']" />

      <base-icon
        class="icon"
        :icon-name="mode + '-icon'"
        width="24"
        height="24"
        :style="colorMode === mode ? '' : 'opacity:.4'"
      >
        <component :is="mode + '-icon'"></component>
      </base-icon>
    </div>
  </div>
</template>

<script>
import DarkIcon from '@/components/icons/DarkIcon.vue'
import LightIcon from '@/components/icons/LightIcon.vue'

export default {
  components: {
    DarkIcon,
    LightIcon
  },
  data() {
    return {
      modes: ['dark', 'light']
    }
  },
  computed: {
    colorMode () {
      return this.$colorMode.preference
    }
  }
}
</script>

<style scoped>
.tab {
  width: 32px;
  height: 32px;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
}
.tab.inactive:hover {
  cursor: pointer;
}

.background-tab {
  width: 100%;
  height: 100%;
  position: absolute;
  background-color: #858597;
}

.icon {
  z-index: 5;
}

.background-tab.active {
  background-color: #424278;
}

.background-tab.left {
  border-radius: 3px 0 0 3px;
}

.background-tab.right {
  border-radius: 0 3px 3px 0;
}
</style>
