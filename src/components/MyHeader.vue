<template>
  <div class="header">
    <div class="layer">
        <div class="container">
            <nav class="flex">
                <!-- Logo Image -->
                <div class="logo">
                    <img src="@/assets/img/theme_eduprime_logo.png" alt="Logo Eduprime">
                </div>

                <!-- Actions -->
                <ul class="actions-wrapper flex">
                    <li class="action" v-for="(items, index) in navListArray" :key="index">
                        <a class="single-action flex" href="#"> {{items.title}} <i v-if="items.arrowActive" class="fa-solid fa-caret-down arrow"></i></a>
                    </li>

                    <div class="button">
                        <a class="btn btn-yellow" href="#">VIEW COURSES</a>
                    </div>
                </ul>
            </nav>
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

.header {
    // background-color: $bgJumboColor;
    background-image: url('@/assets/img/theme_slider2_bg-1.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    height: 500px;

    .layer {
        background-color: $mainColor;
        height: 500px;
        opacity: 0.94;
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
}
</style>