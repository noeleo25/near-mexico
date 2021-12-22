<template>
  <div class="tabs d-flex align-items-center mx-auto">
    <div
      :class="['tab', activeTab == 2 ? 'inactive' : '']"
      @click="activeTab = 1"
    >
      <div :class="['background-tab left', activeTab == 1 ? 'active' : '']" />
      <base-icon
        class="moon-icon icon"
        icon-name="moon-icon"
        width="24"
        height="24"
        :style="activeTab == 2 ? 'opacity:.4' : ''"
      >
        <MoonIcon />
      </base-icon>
    </div>
    <div
      :class="['tab', activeTab == 1 ? 'inactive' : '']"
      @click="activeTab = 2"
    >
      <div :class="['background-tab right', activeTab == 2 ? 'active' : '']" />
      <base-icon
        class="sun-icon icon"
        icon-name="sun-icon"
        width="24"
        height="24"
        :style="activeTab == 1 ? 'opacity:.4' : ''"
      >
        <SunIcon />
      </base-icon>
    </div>
  </div>
</template>

<script>
import MoonIcon from '@/components/icons/MoonIcon.vue'
import SunIcon from '@/components/icons/SunIcon.vue'

export default {
  components: {
    MoonIcon,
    SunIcon
  },
  data () {
    return {
      activeTab: 1
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
  border-radius: 5px 0 0 5px;
}

.background-tab.right {
  border-radius: 0 5px 5px 0;
}
</style>
