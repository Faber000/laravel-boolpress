<template>
  <div class="card">
    <h2>{{title}}</h2>
    <div>{{content}}</div>
    <router-link :to="{ name: 'single-post', params: {slug: slug} }">Leggi di più</router-link>
  </div>
</template>

<script>
export default {
    name: 'BaseCard',
    props: {
        title: {
            type: String
        },
        slug: {
            type: String,
        },
        content: {
            type: String
        },  
    }
}
</script>

<style lang="scss" scoped>

.card {
    background-color: white;
    padding: 10px;
}
</style>