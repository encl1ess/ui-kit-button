<template>
    <div class="timer" ref="timer">
        {{ timeWithZeros }}
    </div>
</template>

<script>
export default {
    data() {
        return {
            isCounting: false,
            minutes: 0,
            seconds: 0,
            time: 0,
            myTimer: null

        }
    },
    props: {
        timer: String
    },
    computed: {
        timeWithZeros() {
            let time = this.time/60;
            let minutes = parseInt(time);
            let seconds =  Math.round((time - minutes) * 60);
            return `${this.getZero(minutes)}:${this.getZero(seconds)}`;
        },

    },
    mounted() {
        let [minutes, seconds] = this.timer.split(":").map(elem => parseInt(elem));
        this.minutes = minutes;
        this.seconds = seconds;
        this.time = this.minutes * 60 + this.seconds;
        this.isCounting = true;
        if (!this.myTimer) {
            this.myTimer = setInterval(() => {
                if (this.time > 0) {
                    this.time--

                } else {
                    clearInterval(this.myTimer);
                    this.isCounting = false;
                    this.$refs.timer.style.display = 'none';
                    this.$emit('endTimer', this.isCounting)
                }
            }, 1000)


        }
    },
    methods: {
        getZero(num) {
            if (num >= 0 && num < 10) {
                return `0${num}`;
            } else return num;
        },

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