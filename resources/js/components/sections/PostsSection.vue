<template>
  <section class="posts">
    <div class="container">
        <div class="row">
            <div class="col mb-5" v-for="post in posts" :key="post.slug">
                <BaseCard :title="post.title" :slug="post.slug" :content="post.content"/>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
import BaseCard from '../common/BaseCard.vue';
export default {
    name: 'PostsSection',
    data() {
        return {
            posts: []
        };
    },

    components: {
        BaseCard,
    },

    created() {
        axios.get('/api/posts')
        .then((response) => {
            this.posts = response.data;
        })
        .catch((e) => {
            console.log(e);
        });
    },
}
</script>

<style lang="scss" scoped>

</style>