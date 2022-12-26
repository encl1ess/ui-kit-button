<template>
    <button class="custom-button" :type="type">
        <slot name="icon"></slot>
        <slot></slot>
        <slot name="timer"></slot>
    </button>

</template>

<script>
export default {
    name: 'custom-button',
    props: {
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
            type: Boolean,
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
    padding: 0 2rem;
}

@mixin disabled-view {
    background-color: $disabled;
    color: #767679;
    path[fill] {
        color: red;
    }
}

@import url('https://fonts.googleapis.com/css2?family=Nunito:ital,wght@0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;0,1000;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900;1,1000&display=swap');

.custom-button {
    font-family: 'Nunito';
    text-transform: uppercase;
    font-weight: 1000;
    font-size: 18px;
    line-height: 24px;
    text-align: center;
    color: #ffffff;
    border: none;
    border-radius: 1.5rem;
    padding: 0 1.6rem;
    // vertical-align: middle;
    height: $normal;

    &[small] {
       @include small-size;

    }

    &[normal] {
        height: $normal;
        padding: 0 3rem;
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
}


</style>