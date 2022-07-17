<template>
  <section>
    <div class="small-container">
        <!-- Latest Courses -->
        <div class="latest-courses">
            <div class="title">
                <h2>Latest Courses</h2>
            </div>

            <!-- Cards -->
            <ul class="flex">
                <li v-for="(course, index) in latestCourses" :key="index" class="single-course flex">
                    <!-- Icon -->
                    <div class="icon">
                        <img :src="require(`@/assets/Icons/${course.icon}`)" :alt="course.title">
                    </div>

                    <!-- Title -->
                    <div class="title">
                        <h3>
                            {{course.title}}
                        </h3>
                    </div>

                    <!-- Teacher Assigned -->
                    <div class="teacher-assigned">
                        <span>Teacher: </span>
                        <span>{{course.teacher}}</span>
                    </div>

                    <div class="price-course">
                        <span>Price: </span>
                        <span>{{course.price}}</span>
                    </div>

                    <div class="button">
                        <a class="btn btn-pink" href="#">
                            <span>
                                <!-- icon -->
                                View Course
                            </span>
                        </a>
                    </div>
                </li>
            </ul>
        </div>

        <!-- Method  -->
        <div class="method">

            <!-- Main Content -->
            <div class="flex">
                <div class="left-side">

                    <!-- Icon Deplayed up to the Title -->
                    <div class="icon">
                        <img src="@/assets/Icons/Exam-icon.png" alt="">
                    </div>

                    <!-- Title -->
                    <div class="title">
                        <h2>The most efficient examination method</h2>
                    </div>

                    <div class="text">
                        <p>
                            EduPrime has gathered teachers from around the globe to brainstorm in order to facilitate thje evolution of our students. Every teacher from our university has an influence on how students are evaluated at his/her subject.
                        </p>
                    </div>

                    <div class="button">
                        <a class="btn btn-pink" href="#">
                            <span>Browse through courses</span>
                        </a>
                    </div>
                </div>

                <!-- Right Side -->
                <div class="right-side flex">
                    <img src="@/assets/img/Exam-Illustration.png" alt="">
                </div>
            </div>
        </div>

        <!-- Internationa Students  -->
        <div class="international-students">

            <!-- Main Content -->
            <div class="flex">
                <div class="left-side flex">
                    <img src="@/assets/img/Girl-Illustration.png" alt="">
                </div>

                <!-- Right Side -->
                <div class="right-side">
                   
                    <!-- Icon Deplayed up to the Title -->
                    <div class="icon">
                        <img src="@/assets/Icons/Exam-icon-1.png" alt="">
                    </div>

                    <!-- Title -->
                    <div class="title">
                        <h2>Variables fees for international students</h2>
                    </div>

                    <div class="text">
                        <p>
                            EduPrime has gathered teachers from around the globe to brainstorm in order to facilitate thje evolution of our students. Every teacher from our university has an influence on how students are evaluated at his/her subject.
                        </p>
                    </div>

                    <div class="button">
                        <a class="btn btn-pink" href="#">
                            <span>List of Fees</span>
                        </a>
                    </div>
                </div>
            </div>
        </div>

    </div>
  </section>
</template>

<script>
export default {
    name: 'SectionFour',
    props: {
        latestCourses: Array
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';

section {
    padding: 50px 0;
}

.latest-courses {
    ul {
        li {
            flex-direction: column;
            align-items: center;
            box-shadow: 1px 1px 20px rgba(128, 128, 128, 0.176);
            width: calc(100% / 4);
            margin:50px 15px;
            padding: 30px 20px 50px 20px;
            text-align: center;
            position: relative;

            &:nth-child(1){
                margin-left: 0;
            }

            &:nth-child(4) {
                margin-right: 0;
            }

            .icon {
                img {
                    width: 60px;
                }
            }

            .teacher-assigned{
                padding: 7px 0;
            }

            .teacher-assigned span:first-child, .price-course span:first-child {
                color: rgb(150, 146, 146);
            }

            .teacher-assigned span:last-child, .price-course span:last-child {
                font-weight: 700;
            }

            span{
                font-size: 13.5px;
            }

            .title h3{
                font-size: 17px;
                color: $mainTextColor;
                padding-top: 15px;
            }

            .btn {
                position: absolute;
                padding: 10px 0;
                bottom: -15px;
                left: 50%;
                transform: translate(-50%);
                width: 130px;

                span {
                    // font-size: 11px;
                }
            }
        }
    }
}

.method {
    padding: 70px 0;

    
    .icon {
        margin-bottom: 20px;

        img {
            width: 50px;
        }
    }

    // Left Side
    .left-side {
        width: 50%;
        .text {
            padding: 30px 0;
        }

        .btn {
            padding: 23px 40px;
        }
        
        p {
            width: 95%;
        }
    } 

    // Right Side
    .right-side {
        width: 50%;
        align-items: center;
        justify-content: flex-end;

        img {
            padding-left: 70px;
            max-width: 540px;
        }
    }
}

.international-students {
    padding: 70px 0;

    .icon {
        margin-bottom: 20px;

        img {
            width: 50px;
        }
    }

    .left-side {
        width: 50%;
        align-items: center;
        img {
            padding-right: 70px;
            max-width: 540px;
        }
    }

    .right-side {
        width: 50%;
         .text {
            padding: 30px 0;
        }

        .btn {
            padding: 23px 40px;
        }

        .btn-pink {
            transition: 0.3s;
        }

        .btn-pink:hover {
            background-color: $mainButtonColor;
        }

        p {
            width: 95%;
        }
    }

}

</style>