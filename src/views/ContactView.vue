<template lang="">
     <div>
           <h1>
            these are our contacts
           </h1>
        </div>
    <div>
        <section v-for="contact in contacts" :key="contact.value">
            
                {{contact.email}} | {{contact.number}} |   {{contact.facebook}} | {{contact.twitter}}  
             
        </section>
    </div>
    <contact-comp/>
</template>
<script>
import ContactComp  from "../components/ContactComp.vue";
export default {
    data(){
        return{
            contacts : [
            {email:'olwe2tcpipv4@duck.com',number:'07123456789' ,facebook:'abc def',twitter:'uikjwiol vcx'},
            {email:'alwe1tcpipv4@duck.com',number:'08123456789' ,facebook:'fds def',twitter:'erfdews vcx'},
            {email:'aphiwe5tcpipv4@duck.com',number:'02123456789' ,facebook:'hjk def',twitter:'yghjiolk vcx'},
            {email:'okwe6tcpipv4@duck.com',number:'03123456789' ,facebook:'njk def',twitter:'ujnbghy vcx'},

            ]
        }
    },
    components:{
        ContactComp
    }
}
</script>
<style scoped>
    div{
        background-image: url("https://static.vecteezy.com/system/resources/previews/023/025/675/non_2x/fantasy-pink-unicorn-background-with-clouds-and-stars-pastel-color-sky-magical-landscape-abstract-fabulous-pattern-cute-candy-wallpaper-vector.jpg");
        background-size: cover;
    }
</style>