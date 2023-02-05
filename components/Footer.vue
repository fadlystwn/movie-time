<template>
  <footer class="bg-gray-900 text-white p-4 bottom-0 w-full">
    <div class="container mx-auto flex flex-col md:flex-row justify-between items-center">
      <p class="text-white text-center md:text-left">&copy; {{ currentYear }} All Rights Reserved.</p>
      <img src="your-logo-url.png" alt="logo" class="h-12" />
      <p class="text-white text-center md:text-right">Made with &hearts;</p>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  data() {
    return {
      currentYear: new Date().getFullYear()
    }
  }
}
</script>