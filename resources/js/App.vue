<template>
    <h1 class="container text-light">My first laravel & vueJS</h1>
</template>

<script>
export default {
    name: 'app',

    data(){

        return{
            apiUrl: '/api/posts',
            posts: null
        }
    },
    methods:{

        getApi(){
            axios.get(this.apiUrl)
            .then(res => {

                this.posts = res.data.posts;

            })
        }

    },

    mounted(){
        this.getApi()
    }
}
</script>

<style>
/* @import  */


</style>
