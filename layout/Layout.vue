<template>
    <div class="bg-gray-800 text-white">
        <Navigation />
        <slot></slot>
        <Footer />
    </div>
</template>

<script>
import Footer from '../components/Footer.vue'
export default {
    name: 'Layout',
    components: { Footer }
}
</script>