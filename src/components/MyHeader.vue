<template>
    <div class="header">
        <div class="layer">

            <div class="container">
                <!-- Nav Section -->
                <nav class="flex">
                    <!-- Logo Image -->
                    <div class="logo">
                        <img src="@/assets/img/theme_eduprime_logo.png" alt="Logo Eduprime">
                    </div>

                    <!-- Actions -->
                    <ul class="actions-wrapper flex">
                        <li class="action" v-for="(items, index) in navListArray" :key="index">
                            <a class="single-action flex" :href="`${items.href}`"> {{items.title}} <i v-if="items.arrowActive" class="fa-solid fa-caret-down arrow"></i></a>
                        </li>

                        <div class="button">
                            <a class="btn btn-yellow" href="#">VIEW COURSES</a>
                        </div>
                    </ul>
                </nav>

                <!-- Jumbotron Section -->
                <div class="jumbotron">
                    <div class="title">
                        <h1>Key to your success</h1>
                    </div>
                    <p>
                        EduPrime is the most versatile WordPress theme for educational purposes, showcasing universities, courses, secondary schools etc.
                    </p>

                    <div class="button-choose flex">
                        <div class="search-course">
                            <a class="btn btn-yellow" href="#"> <i class="fa-solid fa-magnifying-glass"></i> Search courses</a>
                        </div>
                        <div class="apply-university">
                            <a class="btn btn-white" href="#"><i class="fa-solid fa-user-plus"></i> Apply for universitys</a>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Left Small quick Menu -->
            <div class="quick-action">
                <div class="cart">
                    <a href="#"><i class="bi bi-cart3"></i></a>
                </div>
                <div class="book">
                    <a href="#"><i class="bi bi-book"></i></a>
                </div>
                <div class="palette">
                    <a href="#"><i class="bi bi-palette2"></i></a>
                </div>
            </div>

            <div class="wave">
                </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'MyHeader',
    props: {
        navListArray: Array
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';

.wave {
    background-image: url('@/assets/Waves/Wave-1.png');
    height: 150px;
    background-repeat: no-repeat;
    background-position: left 0 right 0;
    background-size: cover;
    position: absolute;
    bottom: 0;
    width: 100%;
}

.header {
    background-image: url('@/assets/img/theme_slider2_bg-1.jpg'), url('@/assets/Waves/Wave-1.png');
    background-repeat: no-repeat;
    background-size: cover;
    height: 500px;

    .layer {
        background-color: #e95e5ee1;
        height: 550px;
        position: relative;
        
    }
    nav {
        font-size: 13px;
        font-family: $titlesFont;
        color: $secondColor;
        height: 110px;
        align-items: center;
        justify-content: space-between;
        .logo {
            
            img {
                width: 190px;
            }
        }

       ul {
        align-items: center;
        
            li {
                padding-left: 30px;
            }

            .button {
                margin-left: 25px;

                a {
                    transition: 0.5s;
                }

                a:hover {
                    background-color: $secondColor;
                    color: $mainColor;
                }
            }

            a:hover {
                color: $mainButtonColor;
            }

           .single-action {
                align-items: center;
                
                .arrow {
                    font-size: 8px;
                    padding-left: 5px;
                }
           }
       }
    }

    .jumbotron {
        text-align: center;
        color: $secondColor;
        padding: 40px 0;

        h1{
            font-size: 40px;
            color: secondColor;
        }

        p {
            width: 40%;
            margin: 0 auto;
            line-height: 25px;
            font-weight: 100;
            padding: 20px 0;
            font-size: 13px;
        }

        .button-choose {
            justify-content: center;

            .btn {
                margin: 0 10px;
            }

            .fa-solid {
                padding-right: 5px;
            }
        }

    }

    .wave {
        // position: absolute;
        // bottom: 0;
    }

    .quick-action {
        font-size: 12px;
        width: 30px;
        background-color: $mainButtonColor;
        border-radius: 3px;
        position: absolute;
        top: 40%;
        left: -7px;
        box-shadow: 2px 1px 10px rgba(0, 0, 0, 0.412);

        .cart, .book, .palette {
            padding: 7px 0;
        }

        a {
            color: white;
            margin: 12px;
           
        }
    }
}
</style>