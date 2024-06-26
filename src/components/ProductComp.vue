<template lang="">
    <div  :style="{
        backgroundImage:`url(${cover})`,
        backgroundSize:'cover',
        filter: 'blur(4px)'

    }">

    </div>
        <div>
        <h1>This is a product comp</h1> 
        <!-- {{bookTitle}} -->
                <!-- {{bookTitle.title}}
                <br>
                {{bookTitle.author}}
                <br>
                {{bookTitle.year}}
                <br>
                {{bookTitle.pages}}
                <br>
                {{bookTitle.bublisher}}
                <br>
                {{bookTitle.isbn}}
                <br>
                <img :src="bookTitle.cover"> -->

                <slot name ="heading"></slot>
                <slot name ="author"></slot>
                <slot name ="pages"></slot>
                <slot></slot>
        </div>
</template>
<script>

export default {
    // props:['bookTitle']
    props:["cover"]
    
}
</script>
<style scoped>
    /* img{
        width:280px;
        height:280px;
        border-radius: 10%;
    } */
    div{
        width:300px;
        height: 400px;
        position:absolute;
        border-radius: 10%;
    }
    /* h1{
        color:white;
        text-shadow:3px 3px black

    } */
</style>