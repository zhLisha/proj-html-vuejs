<template>
    <section>
        <!-- Top Wave -->
        <svg class="wave-top" xmlns="http://www.w3.org/2000/svg" version="1.0" width="2954.667" height="186.667" viewBox="0 0 2216 140"><path class="st0" d="M324.7 34.8c-76.4 51.8-134.1 82-177.2 92.8-12.2 3.1-33.8 4.3-42.8 2.5-8.1-1.7-18.5-7.2-24.2-12.8-5.7-5.7-10.1-12.2-17.4-26.1C57 79.6 52.6 75 47.7 75c-7.9 0-21.2 9.9-37.9 28.3L0 114v26h1105.2c729.3 0 1104.9-.3 1104.2-1-2.6-2.6-29.5-18-42.9-24.5-46.4-22.7-82.1-27.7-122.7-17.5-4.6 1.2-19.1 5.5-32.3 9.5-40.2 12.4-58.5 16.1-85.5 17.2-33.9 1.3-73.5-5.3-117.9-19.9-14.8-4.8-48.5-17.8-59.7-23l-5.2-2.4-16.3 1.8c-125.9 13.6-219.6 20.5-324.9 23.9-40.1 1.3-166.2.6-196-1-71.9-4-119.7-8.4-173.5-16.2-26.8-3.8-69.6-11.2-83.1-14.4-5-1.1-8-1.3-13.2-.5-3.7.5-18.8 2.3-33.7 3.9C793 88.1 702 89.1 622 79c-51.2-6.5-89.6-15.2-150.5-34-35.4-10.9-84.3-20.7-121.8-24.3-3.5-.3-5.6.9-25 14.1z" fill="#e56768"/></svg>

        <!-- Main Content -->
        <!-- University Time Oriantation -->
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

            <!-- Upcoming Events -->
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
                <div class="sessions">
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
                </div>

                <!-- View All Event -->
                <div class="button">
                    <a class="btn btn-yellow" href="#">
                        <span>View All Events</span>
                    </a>
                </div>

            </div>
        </div>

        <!-- Bottom Wave -->
        <svg class="wave-bottom" xmlns="http://www.w3.org/2000/svg" version="1.0" width="2821.333" height="177.333" viewBox="0 0 2116 133"><path class="st0" d="M6 .4c0 .8 22.8 14.1 35.5 20.7 35.6 18.6 68.6 26.7 96.8 23.9 15.1-1.5 29.4-4.8 54.3-12.6 40-12.5 57.6-16.1 84.4-17.1 45.6-1.6 98.7 10.6 160.6 37.1 7.1 3.1 14.2 5.6 15.8 5.6 1.5 0 17.3-1.6 35-3.5 85-9.2 166.6-15.4 259.1-19.7 36.9-1.7 181.6-1.7 215 0 89.4 4.7 163.2 12.9 226.5 25.4 13.3 2.6 24.2 4.3 28.5 4.2 3.9 0 19.4-1.4 34.5-3.2 60.9-7 102.4-9.6 157-9.6 94.2 0 162.8 9.8 244 34.9 44.3 13.6 79.7 21.3 119.4 25.9l13 1.5 30.5-20.3c85.2-56.8 141.9-83.5 181.6-85.3 28.4-1.3 43 7.9 57 35.7 7.9 15.7 12 19.4 19.5 17.1 6.8-2 15.6-8.9 28.9-22.7l13.1-13.6V0H1061C480.8 0 6 .2 6 .4z" fill="#e56768"/></svg>
    </section>
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

section {
    position: relative;
    margin: 120px 0;

    .wave-top {
        position: absolute;
        bottom: 99.8%;
    }

    .wave-bottom {
        position: absolute;
        top: 99.8%;
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
    padding: 70px 0;
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
                margin-left: 60px;
            }

            .evolution {
                margin-left: 25px;
            }
        }
    }
}

</style>