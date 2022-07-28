<template>
    <div>
        <BaseHeader/>
        <BaseMain/>
    </div>
</template>

<script>
import BaseHeader from '../components/macro/BaseHeader.vue'
import BaseMain from '../components/macro/BaseMain.vue'

export default {
    name: 'App',
    components: {
        BaseHeader,
        BaseMain,
  },
}
</script>

<style scoped>
</style>
