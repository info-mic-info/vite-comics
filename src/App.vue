<script>
import AppHeader from './components/AppHeader.vue'
import AppContent from './components/AppContent.vue'
import AppFooter from './components/AppFooter.vue'
export default {
  components: {
    AppHeader,
    AppContent,
    AppFooter
  }
}
</script>

<template lang="">

 <AppHeader />
 <AppContent />
 <AppFooter />

</template>
<style lang="scss">
@use './styles/generals.scss' as *;
</style> 