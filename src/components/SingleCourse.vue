<template>
    <section class="card">
        <img :src="getImagePath(course.img)" :alt="course.title">
        <h1>
            {{ course.title }}
        </h1>
        <p>
            {{ course.description }}
        </p>
        <p class="price">
            {{ course.price }}
        </p>
        <button>
            View More
        </button>
    </section>
</template>
    
<script>
    export default{
        name: 'SingleCourse',
        data(){
            return{
    
            }
        },
        props: {
            course : Object
        },
        methods:{
            getImagePath: function(img) {
                return new URL(`../assets/img/${img}`, import.meta.url).href;
            },
        }
    }
</script>
    
<style lang="scss" scoped>
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variables.scss' as *;
    section.card{
        height: 520px;
        text-align: center;
        margin: 0 1.5rem;
        box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px, rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
        img,
        h1,
        p{
            margin-bottom: 1.3rem;
        }
        h1,
        p{
            padding: 0 1.5rem;
        }
        img{
            width: 100%;
        }
        h1{
            font-size: $FontSizeML;
        }
        h1:hover{
            color: $yellowColor;
        }
        p{
            font-size: $FontSizeM;
            font-weight: 300;
        }
        p.price{
            font-weight: 600;
            font-size: $FontSizeML;
        }
        button{
            font-size: $FontSizeM;
            background-color: $yellowColor;
        }
        button:hover{
            color: white;
            background-color: $darkGreyColor;
        }
    }
</style>