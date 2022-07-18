<template>
    <section>
        <div class="subsciption small-container flex">
            <div class="title">
                <h2>Subsciption Now to Our Newsletter!</h2>
            </div>
            <div class="input-address" >
                <!-- <form onsubmit="event.preventDefault()"> -->
                <form v-on:submit.prevent>
                    <label for="email-address"> </label>
                    <input v-model="userInput" @keyup.enter="getUserInput()" class="user-input" type="email" placeholder="Email adress..." id="email-address" required>
                    <input class="submit-button" @click="getUserInput()" id="submit" type="image" name="submit" :src="require('@/assets/Icons/paper-plane-solid.png')">
                    <!-- <input class="user-input" type="email" placeholder="Email adress..." id="email-address" required> -->
                    <!-- <input class="submit-button" id="submit" type="image" name="submit" :src="require('@/assets/Icons/paper-plane-solid.png')"> -->
                </form>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'SectionSubscription',
    data() {
        return {
            userInput: null,
            // userInputeSaved: []
        }
    },

    methods: {
        getUserInput() {
            // this.userInputeSaved.push(this.userInput);
            // this.userInput = '';
        }
    }
}
</script>

<style lang="scss" scoped>
@import '@/style/variables.scss';

section {
    background-color: $mainColor;
    height: 150px;
}

.subsciption {
    height: 100%;
    align-items: center;
    justify-content: space-between;
     .title h2{
        color: $secondColor;
        font-size: 30px;
        font-weight: 100;
    }
}

.input-address {
    position: relative;
    .user-input {
        border: none;
        height: 65px;
        width: 450px;
        padding-left: 20px;
        border-radius: 40px;
        vertical-align: middle;
        outline: none;
    }

    .submit-button {
        width: 65px;
        vertical-align: middle;
        position: absolute;
        right: -2.5px;
    }
}

</style>