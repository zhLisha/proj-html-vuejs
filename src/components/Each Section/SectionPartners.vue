<template>
  <section>
    <div class="partners small-container">
        <!-- Title -->
        <div class="title">
            <h2>Partners</h2>
        </div>
        <!-- Description -->
        <div class="text">
            <span>
                Laverage agile frameworks to provide a robust synopsts for hight level overviews. Iterative approaches to corporate strategy.
            </span>
        </div>

        <!-- Partners Icon -->
        <div class="partners-icon">
            <ul class="flex">
                <li v-for="(partners, index) in partnerIcons" :key="index">
                    <a href="#">
                        <img :src="require(`@/assets/Icons/${partners.image}`)" :alt="partners.title">
                    </a>
                </li>
            </ul>
        </div>
    </div>

    <!-- Wave -->
    <div class="wave"></div>
  </section>
</template>

<script>
export default {
    name: 'SectionPartners',
    props: {
        partnerIcons: Array
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';

section {
    background-image: url('@/assets/Waves/background-wave3.png');
    background-repeat: no-repeat;
    transform: rotate(180deg);
    background-size: contain
}
.partners {
    height: 450px;
    text-align: center;
    padding: 50px 0;
    transform: rotate(180deg);

    .text {
        width: 40%;
        margin: 0 auto;
        padding-top: 35px;
    }
}

.partners-icon {
    ul {
        justify-content: space-between;
        flex-wrap: wrap;

        li {
            margin-top: 35px;

            a {
                img {
                    height: 50px;
                    opacity: 0.3;
                }

                &:hover img{
                    opacity: 1;
                }
            }
            
        }
    }
}


</style>