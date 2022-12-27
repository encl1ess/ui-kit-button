<template>
    <div class="timer">
        {{ time }}
    </div>
</template>

<script>
export default {
    data() {
        return {
            isCounting: false,
            minutes: 0,
            seconda: 0,
            time: ''

        }
    },
    props: {
        timer: String
    },
    computed: {
        timeWithZeros() {

        }

    },
    methods: {
        getZero(num) {
            if (num >= 0 && num < 10) {
                return `0${num}`;
            } else return num;
        },
        start() {
            this.isCounting = true;

        }

    }
}
</script>

<style lang="scss" scoped>
.timer {
    color: #FFFFFF;
    background: #DF3F3E;
    width: 54px;
    height: 26px;
    border-radius: 0.8rem;
    font-size: 16px;
}
</style>