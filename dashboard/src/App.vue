<template>
  <modal-factory />
  <router-view />
</template>
<script>
import ModalFactory from './components/ModalFactory/ModalIndex.vue'
export default {
  components: { ModalFactory }
}
</script>
