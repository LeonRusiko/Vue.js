<script>
    export default {
        data () {
            return {
                counter: 0,
            } 
        },
        methods: {
           Like(){
            this.counter++
        },

        },
        
    }
</script>

<template>
    <div>
       <div class="button" @click="Like">
        Likes:{{counter}}
    </div>

    </div>
</template>

<style scoped>
.button{
    width: 100px;
    padding: 5px;
    border: 1px solid black;

    display: flex;
    justify-content: center;
    cursor: pointer;
}
</style>