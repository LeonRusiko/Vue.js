<script>
export default {
    data() {
        return {
            post: {
                disable: true
            }
        }
    },
    methods: {
        disableChange(){
            this.post.disable = !this.post.disable
            console.log(this.post)
        },
        changeFont (event){
            this.post.fontSize = event.target.value + "px"
        }
    }
}
</script>


<template>
      <div class="post">
        <textarea :disabled="post.disable" class="postText" :style="{backgroundColor: post.backColor, color: post.fontColor, fontSize: post.fontSize, fontWeight: post.fontWeight, fontStyle: post.fontStyle, fontFamily: post.fontFamily}" name="test" id="" cols="30" rows="10" v-model="post.data"></textarea>
        <input @click="disableChange" type="button" value="Редактировать">
        <div class="editInputs" :class="{visible: post.disable}">
            <p>Color</p>
            <input type="color" name="" id="" v-model="post.fontColor">
            <p>Background-color</p>
            <input type="color" name="" id="" v-model="post.backColor">
            <p>Font-family</p>
            <select name="" id="" v-model="post.fontFamily">
                <option value="Arial">Arial</option>
                <option value="Courier">Courier</option>
                <option value="Verdana">Verdana</option>
            </select>
            <p>Font-size</p>
            <input type="number" name="" id="" @input="changeFont" value="14">
            <p>Font-style</p>
            <select name="" id="" v-model="post.fontStyle">
                <option value="normal">Normal</option>
                <option value="italic">Italic</option>
                <option value="oblique">Oblique</option>
            </select>
    
        </div>
    </div>
</template>

<style>
    *{
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    .post{
        padding: 10px;
        width: 300px;
    }
    .editInputs{
        padding: 10px;
        border: 1px solid black;
    }
    .visible{
        display: none;
    }
</style>