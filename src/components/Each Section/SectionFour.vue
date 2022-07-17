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

</style>