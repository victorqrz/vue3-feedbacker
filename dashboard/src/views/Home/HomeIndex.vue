<template>
  <custom-header @create-account="handleLogin" @login="handleLogin" />
  <contact />
  <footer class="flex justify-center py-10 bg-brand-gray">
    <p class="font-medium text-center text-gray-800">Feedbacker &copy; 2022</p>
  </footer>
</template>

<script>
import { onMounted } from 'vue'
import { useRouter } from 'vue-router'
import Contact from './HomeContact.vue'
import CustomHeader from './CustomHeader.vue'
export default {
  components: { Contact, CustomHeader },
  setup() {
    const router = useRouter()

    onMounted(() => {
      const token = window.localStorage.getItem('token')
      if (token) {
        router.push({ name: 'Feedbacks' })
      }
    })

    function handleLogin() {}

    function handleAccountCreate() {}

    return {
      handleLogin,
      handleAccountCreate
    }
  }
}
</script>
