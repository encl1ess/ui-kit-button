<template>
    <a v-if="type === 'link'" class="custom-link" :href=url>
        <slot></slot>
    </a>
    <button v-else ref="button" class="custom-button" :type="type">
        <div class="wrapper">
            <slot></slot>
        </div>
        <custom-timer v-if="timer" :timer="timer" />
    </button>
</template>

<script>
import CustomTimer from '@/components/CustomTimer.vue';
export default {
    name: 'custom-button',
    components: {
        CustomTimer
    },
    data() {
        return {
            counter: 0,
        }
    },
    props: {
        url: String,
        type: {
            type: String,
            default: 'button',
            validator: (value) => {
                return [
                    'link',
                    'button'
                ].indexOf(value) >= 0
            }
        },
        timer: {
            type: String,
            required: false
        }
    }
}
</script>

<style lang="scss" scoped>
$small: 52px;
$normal: 60px;
$primary: #702C7E;
$secondary: #C4296C;
$success: #6DD1B0;
$warning: #F4BA46;
$disabled: #EFEFEF;
$info: #0083B6;
$danger: #DF3F3E;
$action: #ED732E;

@mixin small-size {
    height: $small;
    border-radius: 1.1rem;
    padding: 0 3rem;
}

@mixin disabled-view {
    background-color: $disabled;
    color: #767679;

}

@import url('https://fonts.googleapis.com/css2?family=Nunito:ital,wght@0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;0,1000;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900;1,1000&display=swap');

.custom-link,
.custom-button {
    font-family: 'Nunito';
    text-align: center;
    color: #ffffff;
    margin: 1rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    cursor: pointer;
}

.custom-link {
    text-decoration: underline;
    font-weight: 700;
    font-size: 16px;
    line-height: 18px;

    &:hover {
        color: #767679;
    }

    &:visited {
        color: #C4296C;

        &:hover {
            color: #767679;
        }
    }
}

.custom-button {

    text-transform: uppercase;
    font-weight: 1000;
    font-size: 16px;
    line-height: 24px;
    border: none;
    border-radius: 1.5rem;
    padding: 0 4rem;
    background: transparent;
    height: $normal;
    flex-wrap: nowrap;

    &[icon] {
        padding: 0 1rem;

        .wrapper {
            width: 30px;
        }
    }

    .wrapper {
        height: 30px;
    }

    .wrapper {
        display: flex;
        align-items: center;
        justify-content: stretch;
        flex-wrap: nowrap;
        flex-shrink: 1;
        height: 30px;
        width: max-content;
    }

    .timer {
        margin-left: 0.5rem;
    }

    &:hover {
        box-shadow: rgba(255, 255, 255, 0.5) 0px 4px 8px -2px, rgba(255, 255, 255, 0.5) 0px 0px 0px 1px;
    }

    &[small] {
        @include small-size;

        &[icon] {
            padding: 0 1rem;

            .wrapper {
                width: 24px;
            }
        }

        .wrapper {
            height: 24px;
        }

    }

    &[normal] {
        height: $normal;
        padding: 0 3rem;

        &[icon] {
            padding: 0 1rem;

            .wrapper {
                width: 30px;
            }
        }

        .wrapper {
            height: 30px;
        }
    }

    &[primary] {
        background-color: $primary;
    }

    &[secondary] {
        background-color: $secondary;

    }

    &[success] {
        background-color: $success;
    }

    &[warning] {
        background-color: $warning;
    }

    &[disabled] {
        @include disabled-view;

        .wrapper {
            color: #767679;
        }
    }

    &[info] {
        background-color: $info;
    }

    &[danger] {
        background-color: $danger;
    }

    &[action] {
        background-color: $action;
    }

    @media (max-width: 640px) {
        @include small-size;
        &[icon] {
            padding: 0 1rem;

            .wrapper {
                width: 24px;
            }
        }
        .wrapper {
            height: 24px;
        }
    }
}
</style>