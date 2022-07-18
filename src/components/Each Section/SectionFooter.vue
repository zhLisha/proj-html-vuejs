<template>
  <footer>
    <section class="small-container flex">
        <!-- Column 1 (Logo + Social)-->
        <div class="logo-social">
            <img src="@/assets/img/theme_eduprime_logo.png" alt="">
            <div class="text">
                <span>
                    EduiPrime is the mosr versatile Worpress theme for educational purposes, showcasing universities, coursees, secondary schools etc.
                </span>
            </div>
            <div class="social-icons">
                <ul class="flex">
                    <li >
                        <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                    </li>
                     <li>
                        <a href="#"><i class="fa-brands fa-twitter"></i></a>
                    </li>
                     <li>
                        <a href="#"><i class="fa-brands fa-instagram"></i></a>
                    </li>
                </ul>
            </div>
        </div>

        <!-- Column 2 All list action -->
        <div class="list-action flex">
            <div class="get-eduprime">
                <h4>Get EduPrime</h4>
                <ul class="text">
                    <li v-for="(link, index) in eduPrimeArray" :key="index">
                        <a href="#">
                            {{link.link}}
                        </a>
                    </li>
                </ul>
            </div>
            <div class="networking">
                <h4>Network</h4>
                <ul class="text">
                        <li v-for="(link, index) in networkingArray" :key="index">
                            <a href="#">
                                {{link.link}}
                            </a>
                        </li>
                </ul>
            </div>
        </div>

        <!-- Column 3 (Search Bar + Search Faculties Facility) -->
        <div class="search-area">
            <div class="search-bar">
                <form>
                    <label for="search"> </label>
                    <input class="user-input" v-model="userInputSearch" type="text" placeholder="Search..." id="search">
                    <input class="search-button" id="image" type="image" name="image" :src="require('@/assets/Icons/search-submit.png')">
                </form>
            </div>
            <div class="facility-search flex">
                <div class="title">
                    <h4>Search Categories</h4>
                </div>
                <div class="buttons">
                    <ul class="flex">
                        <li v-for="(link, index) in facilityArray" :key="index" class="button">
                            <a href="#">{{link.link}}</a>
                        </li>
                    </ul>
                </div>
            </div>

            <div class="copy">
                <span>
                    MotherTheme. All Rights reserved.
                </span>
            </div>
        </div>

        <!-- Button Up Page -->
        <button class="return-top" @click="backToTop()" >
            <i class="fa-solid fa-chevron-up"></i>
        </button>
    </section>
  </footer>
</template>

<script>

export default {
    name: 'SectionFooter',
    props: {
        eduPrimeArray: Array,
        networkingArray: Array,
        facilityArray: Array
    },
    data() {
        return {
            userInputSearch: '',
            shevronShowed: false
        }
    },

    methods: {
        backToTop() {
           window.scrollTo(0, 0)
        }
    },
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';

footer {
    background-color: $mainColor;
    height: 400px;
    color: $secondColor;
    position: relative;
}

.small-container {
    height: 100%;
    align-items: center;

    .logo-social,  
    .list-action, 
    .search-area{
        width: calc(100% / 3);
    }
}

.text {
    color: $secondColor;
    font-size: 13px;
    font-weight: 100;
}

.logo-social {
    img {
        width: 230px;
    }

    .text {
        padding: 40px 0;
    }

    .social-icons {
        ul {

            .fa-brands {
                border: 1px solid $mainButtonColor;
                margin-right: 10px;
                width: 50px;
                height: 50px;
                border-radius: 50%;
                line-height: 50px;
                text-align: center;
                
            }
        }
    } 
}

.list-action {
    justify-content: space-evenly;

    h4 {
        font-family: $titlesFont;
        font-weight: 100;
        padding-bottom: 30px;
    }

    li {
        line-height: 30px;
    }
}

.search-bar {
    position: relative;
    .user-input {
        border: none;
        height: 65px;
        width: 100%;
        padding-left: 20px;
        border-radius: 40px;
        vertical-align: middle;
        outline: none;
    }

    .search-button {
        width: 65px;
        vertical-align: middle;
        position: absolute;
        right: -2.5px;
    }
}

.facility-search {
    flex-direction: column;
    align-items: flex-end;

    h4 {
        padding-top: 30px;
        padding-bottom: 15px;
        font-weight: 100;
        font-size: 15px;
    }
    ul {
        flex-wrap: wrap;
        justify-content: flex-end;

        li {
            border: 1px solid $secondColor;
            padding: 7px 10px;
            border-radius: 20px;
            font-size: 10px;
            margin-top: 10px;
            margin-left: 5px;
        }
    }
}

.copy {
    text-align: right;
    padding-top: 20px;
    span {
        color: $mainButtonColor;
        font-size: 12px;
        font-weight: 100;
    }
}

button {
    background-color: $mainButtonColor;
    color: $secondColor;
    border: none;
    cursor: pointer;
    width: 40px;
    height: 40px;
    border-radius: 50%;
    font-size: 15px;
    line-height: 40px;
    position: fixed;
    bottom: 30px;
    right: 30px;
    transition: all 0.5s;
    z-index: 1;
}
</style>