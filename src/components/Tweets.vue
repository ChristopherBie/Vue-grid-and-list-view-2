<template>
    <div>
        <button @click='notifyParent'>display tweets</button>
        <br>
    </div>
</template>

<script>
    export default {
        name: "vue-tweets",
        data() {
            return {
                tweets: [
                    {
                        author: 'James',
                        date: 'Dec 10',
                        text: 'Hello world!'
                    },
                    {
                        author: 'Chris',
                        date: 'Dec 11',
                        text: 'HELLLOOO!!!'
                    },
                    {
                        author: 'Everyone',
                        date: 'Dec 12',
                        text: 'You are muted!'
                    }
                ]
            }
        },
        methods: {
            notifyParent: function() {
                this.$emit('tweetContent', this.tweets);
            }
        }
    }
</script>

<style>
</style>