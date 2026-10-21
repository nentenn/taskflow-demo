<template>
  <f7-toolbar bottom tabbar icons class="app-tabbar">
    <f7-link
      href="/"
      class="app-nav-link"
      :class="{ 'app-link-active': active === 'home' }"
    >
      <span class="app-nav-content">
        <f7-icon f7="house_fill" />
        <span class="app-nav-label">Головна</span>
      </span>
    </f7-link>

    <f7-link
      href="/tasks/"
      class="app-nav-link"
      :class="{ 'app-link-active': active === 'tasks' }"
    >
      <span class="app-nav-content">
        <f7-icon f7="square_list_fill" />
        <span class="app-nav-label">Завдання</span>
      </span>
    </f7-link>

    <f7-link
      href="/about/"
      class="app-nav-link"
      :class="{ 'app-link-active': active === 'about' }"
    >
      <span class="app-nav-content">
        <f7-icon f7="info_circle_fill" />
        <span class="app-nav-label">Про застосунок</span>
      </span>
    </f7-link>
  </f7-toolbar>
</template>

<script setup>
defineProps({
  active: {
    type: String,
    required: true,
  },
});
</script>

<style scoped>
.app-tabbar {
  --f7-toolbar-height: 64px;
  --f7-tabbar-height: 64px;
  --f7-tabbar-icons-height: 64px;
}

.app-tabbar :deep(.toolbar-inner) {
  box-sizing: border-box;
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  align-items: stretch;
  width: 100%;
  max-width: 800px;
  height: 64px;
  left: 0;
  right: 0;
  top: 0;
  margin: 0 auto;
  padding: 0;
}

.app-tabbar :deep(.app-nav-link) {
  box-sizing: border-box;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  min-width: 0;
  height: 64px;
  margin: 0;
  padding: 0;
  color: #64748b;
  text-align: center;
  text-transform: none;
}

.app-nav-content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 5px;
  width: 100%;
  height: 100%;
}

.app-tabbar :deep(.app-nav-content .icon) {
  position: static;
  display: block;
  width: 24px;
  height: 24px;
  margin: 0;
  padding: 0;
  font-size: 22px;
  line-height: 24px;
  text-align: center;
  transform: none;
}

.app-nav-label {
  display: block;
  width: 100%;
  margin: 0;
  padding: 0;
  font-size: 11px;
  line-height: 14px;
  text-align: center;
  white-space: nowrap;
}

.app-tabbar :deep(.app-link-active) {
  color: #2563eb;
}

@media (max-width: 360px) {
  .app-nav-label {
    font-size: 10px;
  }
}
</style>