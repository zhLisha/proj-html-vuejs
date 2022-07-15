<template>
  <section>
     <!-- Purchase frame -->
        <div class="purchase-frame">
            <a href="#">
                <span>Purchase EduPrime on Envalo Market</span>
            </a>
        </div>

        <span class="arrow"></span>

        <!-- Presentation  -->
        <div class="presentation">

            <!-- Detail Wave -->
            <img class="wave" src="@/assets/Waves/home-background.png" alt="">

            <!-- Icon Deplayed up to the Title -->
            <div class="icon small-container">
                <img src="@/assets/Icons/Books-icon.png" alt="">
            </div>

            <!-- Main Content -->
            <div class="small-container flex">
                <div class="left-side">
                    <!-- Title -->
                    <div class="title">
                        <h2>Thousands of courses for any type of student</h2>
                    </div>

                    <div class="text">
                        <p>
                            Aty EduPrime, it doesn't matter what domain you wish to pursue a career in. Here you can find a couse that satisfies your need within a click away and applies for a course in a matter of minutes. EduPrime is ranked as the most versatile univeristy in the world, thanks to the number of courses it provides.
                        </p>
                    </div>

                    <div class="button">
                        <a class="btn btn-yellow" href="#">
                            <span>Browse through courses</span>
                        </a>
                    </div>
                </div>

                <!-- Right Side -->
                <div class="right-side flex">
                    <img src="@/assets/img/Graduation-Illustration.png" alt="">
                </div>
            </div>
        </div>
  </section>
</template>


<script>
export default {
    name: 'SectionOne'
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';

.purchase-frame {
    color: $secondColor;
    background-color: #1a1a1a;
    width: 150px;
    text-align: center;
    border-radius: 3px;
    font-size: 9px;
    font-weight: 100;
    padding: 3px 10px;
    margin-left: 25px;
    position: relative;
}

.arrow {
    border-top: 5px solid #1a1a1a;
    border-right: 5px solid transparent;
    border-left: 5px solid transparent;
    position: absolute;
    left: 95px;
}


.presentation {
    padding: 70px 0;
    position: relative;

    .wave {
        position: absolute;
        top: 0;
    }

    .icon {
        margin-bottom: 20px;

        img {
            width: 50px;
        }
    }

    .small-container {
        align-items: center;

    }

    // Left Side
    .left-side {
        width: 50%;

        .text {
            padding: 30px 0;
        }

        a {
            cursor: pointer;
        }
    } 

    // Right Side
    .right-side {

        justify-content: center;
        width: 50%;
        img {
            width: 400px;
            z-index: 10;
            padding-left: 20px;
        }
    }
}
</style>