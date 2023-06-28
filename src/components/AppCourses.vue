<template>
    <section class="courses">
        <h1>
            Courses
        </h1>
        <p>
            To keep up with the constantly rising standards of play       
        </p>
        <ul>
            <li v-for="course in coursesList">
                <SingleCourse
                    :course = "course"
                />
            </li>
        </ul>
        <button>
            View Other Courses
        </button>
    </section>
</template>
    
<script>
    import SingleCourse from './SingleCourse.vue';
    export default{
        name: 'AppCourses',
        data(){
            return{
                coursesList:[
                    {
                        img: 'mt-2236-home-img1.jpg',
                        title: "Garry Kasparov's Masterclass",
                        description: 'Learn the tips, tricks, and strategies from one of the best masters',
                        price: '$456',
                    },
                    {
                        img: 'mt-2236-home-img2.jpg',
                        title: "Online Chess Lessons for Beginners",
                        description: 'Catered to adult beginners who have a few hours a week to practice',
                        price: '$205',
                    },
                    {
                        img: 'mt-2236-home-img3.jpg',
                        title: "International Chess School Online",
                        description: 'Chess lessons for children and adults held completely online',
                        price: '$356',
                    },
                ]
            }
        },
        components:{
            SingleCourse
        }
    }
</script>
    
<style lang="scss" scoped>
    @use '../styles/partials/mixins.scss' as *;
    @use '../styles/partials/variables.scss' as *;
    section.courses{
        height: 90vh;
        @include flex(column);
        h1,
        p{
            margin-bottom: 1rem;
        }
        h1{
            font-size: $FontSizeL;
        }
        p{
            font-size: $FontSizeML;
            font-weight: 300;
        }
        ul{
            @include flex();
            width: $dimension;
            margin: 2rem 0;
            li{
                width: calc(100% / 3);   
            }
        }
        button{
            font-size: $FontSizeM;
            background-color: white;
            border: 3px solid black;
        }
        button:hover{
            color: white;
            background-color: $darkGreyColor;
            border: 3px solid $darkGreyColor;

        }
    }
</style>