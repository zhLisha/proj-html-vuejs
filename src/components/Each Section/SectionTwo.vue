<template>
<!-- Section 2 Available Falculties-->
  <section>
    <div class="small-container">
        <!-- Text Area -->
        <div class="text-area">
            <div class="title">
                <h2>Faculties available at EdiPrime</h2>
            </div>
            <div class="text">
                <p>
                    A single university with a load of courses, tailored to satisfy any student's needs.
                </p>
            </div>
        </div>
    </div>

     <!-- Avalaible Faculties -->
    <div class="faculties-wrapper">
        <ul class="avalaible-faculties flex small-container">
            <li v-for="(faculties, index) in mainFacultiesArray" :key="index" class="flex" @mouseenter="getCurrentCard(index)">
                <img :src="require(`@/assets/Icons/${faculties.icon}`)" alt="">
                <img class="white-faculties" :src="require(`@/assets/Icons/${faculties.wIcon}`)" :alt="faculties.title">
                <span>{{faculties.faculty}}</span>
            </li>
        </ul>
    </div>

     <!-- Faculties Detail -->
        <div class="faculties-ditail small-container flex" v-for="(details, index) in mainFacultiesArray[currentCard].details" :key="index">
            <div class="left-side flex">
                <img class="faculty-image" :src="require(`@/assets/img/${details.image}`)" :alt="details.title">
            </div>

            <div class="right-side">
                <div class="title">
                    <h2>{{details.title}}</h2>
                    
                </div>
                <div class="text">
                    <p>
                        {{details.text}}
                    </p>
                </div>

                <div class="button">
                    <a href="#" class="btn btn-pink">
                        <span>{{details.button}}</span>
                    </a>
                </div>
            </div>
        </div>
  </section>
</template>

<script>
export default {
    name: 'SectionTwo',
    props: {
        mainFacultiesArray: Array
    },

    data() {
        return {
            currentCard: 0
        }
    },

    methods: {
        // Funzione per assegnare la card Faculty corrente che si sta guardando
        getCurrentCard(index) {
            // Default setto il primo dell'index
            this.currentCard = 0;
            
            this.currentCard = index;
        }
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/common.scss'; 

section {
    padding: 50px 0;
    z-index: 9999;
    .text-area {
        text-align: center;

        p {
            width: 40%;
            margin: 0 auto;
            padding: 25px 0;
        }
    }

    .faculties-wrapper {
        border-top: 1px solid rgba(128, 128, 128, 0.108);
        border-bottom: 1px solid rgba(128, 128, 128, 0.108);
        box-shadow: 1px 1px 10px rgba(128, 128, 128, 0.197);
        .avalaible-faculties {
            li {
                color: $mainColor;
                flex-direction: column;
                align-items: center;
                border: 1px solid rgba(128, 128, 128, 0.144);
                width: calc(100% / 5);
                padding: 30px 0;
                transition: 0.2s;

                .arrow {
                    border-top: 5px solid $mainColor;
                    border-right: 5px solid transparent;
                    border-left: 5px solid transparent;
                    position: absolute;
                    left: 95px;
                    // display: none;
                }

                .default-faculty-card {
                    color: $secondColor;
                    background-color: $mainColor;
                }

                .white-faculties {
                    position: absolute;
                    display: none;

                    // &:after {
                    //     content: '';
                    //     position: relative;
                    //     width: 0;
                    //     height: 75px;
                    //     left: 40%;
                    //     top: -39px;
                    //     border-left: 10px outset transparent;
                    //     border-right: 10px solid transparent;
                    //     border-bottom: 10px solid  $mainColor;
                    // }
                }

                &:hover {
                    color: $secondColor;
                    background-color: $mainColor;
                }

                &:hover .white-faculties{
                    display: block
                }

                span {
                    font-size: 12px;
                    font-weight: 100;
                    padding-top: 15px;
                    font-family: $titlesFont;
                }

                img {
                    width: 70px;
                }

                
            }
        }
    }
    
    .faculties-ditail {
        min-height: 450px;
        padding: 70px 0;
        align-items: center;
        .left-side {
            width: 50%;
            justify-content: center;

            .faculty-image{
                width: 300px;
                margin-right: 50px;
            }
        }

        .right-side {
            width: 50%;

            h2 {
                font-size: 30px;
            }

            .text {
                p{
                    padding: 30px 0;
                    color: #8b8b8abc
                }
            }
        }
    }

}
</style>