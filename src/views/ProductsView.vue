<template lang="">
    <div>
       <h1>this is the products page 👌

       </h1> 
    </div>
       <div>
        <div class='hehe'>
            <section v-for="book in books" :key="book.value">
                <!-- {{book.title}} | {{book.author}} | {{book.year}} | {{book.genre}} -->
                <!-- <product-comp :book-title="book"/> -->
                <product-comp :cover="book.cover">
                    <template #heading>
                        <h1>{{book.title}}</h1>
                    </template>
                    <template #author>
                        <h5>Author: {{book.author}}</h5>
                    </template>
                    <template #pages>
                        <h3>{{book.pages}} Pages</h3>
                    </template>
                    <template #default>
                      {{book.publisher}}
                    </template>
                    
                </product-comp>
                <!-- <product-comp/> -->
            </section>
        </div>
       </div>
</template>
<script>
import ProductComp from '@/components/ProductComp.vue';
export default {
    data(){
        return{
            books:[
            {title: "The Great Gatsby",
            author: "F. Scott Fitzgerald",
            year: 1925,
            genre: "Literary Fiction",
            pages: 180,
            publisher: "Charles Scribner's Sons",
            isbn: "978-0743273565",
            cover:'https://i0.wp.com/americanwritersmuseum.org/wp-content/uploads/2018/02/CK-3.jpg?resize=267%2C400&ssl=1'
            },
            {title: "To Kill a Mockingbird",
            author: "Harper Lee",
            year: 1960,
            genre: "Southern Gothic",
            pages: 281,
            publisher: "J. B. Lippincott & Co.",
            isbn: "978-0446310789",
            cover:'https://media.glamour.com/photos/56e1f3c462b398fa64cbd304/master/w_1600%2Cc_limit/entertainment-2016-02-18-main.jpg'
            },
            {title: "1984",
            author: "George Orwell",
            year: 1949,
            genre: "Dystopian Fiction",
            pages: 328,
            publisher: "Secker & Warburg",
            isbn: "978-0451524935",
            cover:'https://i0.wp.com/www.printmag.com/wp-content/uploads/2017/01/2a34d8_463ff497abfa4bca9b96d696e911746fmv2.jpeg?resize=500%2C769&quality=89&ssl=1'
            },
            {title: "Pride and Prejudice",
            author: "Jane Austen",
            year: 1813,
            genre: "Romance",
            pages: 279,
            publisher: "Thomas Egerton",
            isbn: "978-0141439513",
            cover:'https://cdn.kobo.com/book-images/08ba5a67-f48d-420e-be8e-6de7a73b7d85/1200/1200/False/pride-prejudice-13.jpg'
            },
            {title: "The Catcher in the Rye",
            author: "J.D. Salinger",
            year: 1951,
            genre: "Coming-of-age Fiction",
            pages: 214,
            publisher: "Little, Brown and Company",
            isbn: "978-0316769488",
            cover:'https://cdn.britannica.com/94/181394-050-2F76F7EE/Reproduction-cover-edition-The-Catcher-in-the.jpg'
            }
],
        }
    },
  components:{
    ProductComp 
    
  }
}
</script>
<style scoped>
    section{
        border:3px black solid;
        border-radius: 10%;
        height:400px;
        width: 300px;
        margin:auto;
        color:white;
        text-shadow:3px 3px black
        
    }
    .hehe{
        display: grid;
        grid-template-columns:repeat(5,1fr)
    }
</style>