<template>
    <div v-if="post" class="container">
        <h1>{{post.title}}</h1>
        <p>{{post.content}}</p>
        <p v-if="post.category">Categoria: {{post.category.name}}</p>
        <div class="mt-5">
            <router-link :to="{name: 'home'}">Home Page</router-link>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SinglePost',
    data() {
        return {
            post: null
        }
    },
    created() {
        axios.get(`/api/posts/${this.$route.params.slug}`)
            .then((response) => {
                this.post = response.data;
            })
    }
}
</script>

<style lang="scss" scoped>

</style>