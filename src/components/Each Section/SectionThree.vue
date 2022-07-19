<template>
    <div class="wrapper">
        <!-- University Time Oriantation -->
        <section id="year-program" >
            <div class="main-content">
                <div class="small-container university-year flex">

                    <!-- Icons -->
                    <div class="icon">
                        <img src="@/assets/Icons/Clock-and-Bell.png" alt="">
                    </div>

                    <!-- Title -->
                    <div class="title">
                        <h2>University Year</h2>
                    </div>

                    <!-- Top Text Area -->
                    <div class="text text-top flex">
                        <div class="demo-classes">
                            <div class="title">
                                <h3>Demo Classes</h3>
                            </div>
                            <div class="text">
                                In the first week, students try to accommodate with the teaching style and choose their optional courses.
                            </div>
                        </div>

                        <div class="graduation-day">
                            <div class="title">
                                <h3>Graduation Day</h3>
                            </div>
                            <div class="text">
                                On the day of graduation, all students gather for the ceremony and then network and party among others.
                            </div>
                        </div>
                    </div>

                    <!-- Image Timing Diagram -->
                    <div class="time-diagram">
                        <img src="@/assets/img/Timeline-Item.png" alt="">
                    </div>

                    <!-- Bottom Text Area -->
                    <div class="text text-bottom flex">
                        <div class="orientation">
                            <div class="title">
                                <h3>Orientation</h3>
                            </div>
                            <div class="text">
                                <span>
                                    First day of the university year, all students dather for the opening ceremony and then network with others.
                                </span>
                            </div>
                        </div>

                        <div class="evolution">
                            <div class="title">
                                <h3>Evolution</h3>
                            </div>
                            <div class="text">
                                <span>
                                    Ate the end of semester, students take a general evolution test for every subject they're learning.
                                </span>
                            </div>
                        </div>
                    </div>
                </div>
                
                
            </div>
        </section>

        <!-- Upcoming Events -->
        <section id="section-news" class="sessions">

            <div class="main-content">
                <div class="small-container upcoming-events">

                    <!-- Icon -->
                    <div class="icon">
                        <img src="@/assets/Icons/upcoming-events-calendar-icon.png" alt="">
                    </div>

                    
                    <!-- Title -->
                    <div class="title">
                        <h2>Upcoming Events</h2>
                    </div>

                    <!-- Find Sessions Event -->
                    <ul class="flex">
                        <li v-for="(event, index) in upComingEvent" :key="index" class="single-session">
                            <div class="title">
                                {{event.title}}
                            </div>
                            <div class="text date-event">
                                <i class="bi bi-calendar3"></i>
                                {{event.date}}
                            </div>
                            <div class="text">
                                {{event.details}}
                            </div>
                            <div class="button">
                                <a class="btn btn-pink" href="#">
                                    <i class="fa-solid fa-plus"></i>
                                    <span>Find More</span>
                                </a>
                            </div>
                        </li>
                    </ul>
                            

                    <!-- View All Event -->
                    <div class="button">
                        <a class="btn btn-yellow" href="#">
                            <span>View All Events</span>
                        </a>
                    </div>

                </div>
            </div>
        </section>
    </div>
</template>

<script>
export default {
    name: 'SectionThree',
    props: {
        upComingEvent: Array
    }

}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';

.wrapper {
    padding: 180px 0;
    background-image: url('@/assets/Waves/svg-0.svg'), url('@/assets/Waves/svg-1.svg');
    // background-color: pink;
    background-repeat: no-repeat;
    background-position: top -5px left, bottom 5px left;
}

#year-program {
    .main-content {
        padding-top: 70px;
    }
}

#section-news {
    .main-content {
        padding-bottom: 90px;
    }
}

.university-year {
    flex-direction: column;
    align-items: center;
    padding-bottom: 50px;

    .title {
        h2 {
            background-color: #db2a2c;
            font-size: 50px;
        }
    }

    .text {
        color: $secondColor;
        font-weight: 100;
    }

    .text-top {
        padding: 40px 0 20px 0;
        justify-content: flex-end;

        .text {
            padding-top: 20px;
        }

        .graduation-day {
            width: 35%;
            margin-right: 15px;
        }

        .demo-classes {
            width: 35%;
            margin-right: 45px;
        }
    }

    .text-bottom {
        padding: 20px 0;
        justify-content: flex-start;

        .orientation {
            width: 35%;
            margin-left: 15px;
        }

        .evolution {
            width: 35%;
            margin-left: 45px;
        }
    }
}

.upcoming-events {

    ul.flex{
        justify-content: center;
    }
    .title {

        h2 {
            font-size: 50px;
            padding-bottom: 20px;
        }
    }
    .single-session {
        background-color: $secondColor;
        margin: 15px 15px 80px 15px;
        padding: 20px 20px 50px 20px;
        border-radius: 15px;
        color: $mainTextColor;
        position: relative;

        .title {
            font-size: 23px;
        }

        .text {
            font-size: 13px;
            width: 90%;
            margin: 0 auto;
            opacity: 0.7;
        }

        .date-event {
            padding: 10px 0;
            opacity: 0.7;
        }

        .btn {
            position: absolute;
            bottom: -20px;
            left: 50%;
            transform: translate(-50%);
            box-shadow: 1px 1px 5px rgba(187, 75, 75, 0.818);
            padding: 12px 25px;
        }

        .fa-solid {
            padding-right: 10px;
        }
    }
}

.main-content {
    background-color: $mainColor;
    text-align: center;
    
    .icon {
        margin: 0 auto;
        width: 55px;
    }

    h2 {
        color: $secondColor;
        font-size: 35px;
        margin: 20px 0;
    }

    .btn-yellow {
        transition: 0.3s;
    }

    .btn-yellow:hover {
        background-color: $mainColor;
        box-shadow: 1px 1px 5px rgba(187, 75, 75, 0.818);
        transform: scale(1.1);
    }
    
}

// ************************************
// MEDIA QUERY for year-program details
// ************************************

@media screen and (min-width: 1000px) {
    .university-year {
        .text-top {
            .demo-classes {
                margin-right: 40px;
            }
        }

        .text-bottom {
            .evolution {
                margin-left: 45px;
            }
        }
    }
}
@media screen and (min-width: 1200px) {
    .university-year {
        .text-top {
            .demo-classes {
                margin-right: 50px;
            }
        }

        .text-bottom {
            .evolution {
                margin-left: 55px;
            }
        }
    }
}
@media screen and (min-width: 1350px) {
    .university-year {
        .text-top {
            .demo-classes {
                margin-right: 60px;
            }
        }

        .text-bottom {
            .evolution {
                margin-left: 65px;
            }
        }
    }
}
@media screen and (min-width: 1600px) {
    .university-year {
        .text-top {
            .graduation-day {
                margin-right: 50px;
            }
            .demo-classes {
                margin-right: 20px;
            }
        }

        .text-bottom {
            .orientation {
                margin-left: 35px;
            }

            .evolution {
                margin-left: 45px;
            }
        }
    }
}
@media screen and (min-width: 1800px) {
    .university-year {
        .text-top {
            .graduation-day {
                margin-right: 80px;
            }
            .demo-classes {
                margin-right: 0;
            }
        }

        .text-bottom {
            .orientation {
                margin-left: 80px;
            }

            .evolution {
                margin-left: 0px;
            }
        }
    }
}

</style>