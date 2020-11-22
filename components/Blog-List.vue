<template> 
<section class="features">
    <!-- <article v-for="article in blogPosts">   ...  </article>  -->
    </section>
    </template>
    <script>
        export default {
        props: ['limit'],
        computed: {
            blogPosts: function(){
                return this.$store.state.blogPosts && this.limit && this.$store.state.blogPosts.length > this.limit ? this.$store.state.blogPosts.slice(0, this.limit) : this.$store.state.blogPosts;}
                    }
                }
    </script>