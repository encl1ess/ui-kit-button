<template>
    <div :class="{}">
        <button 
        :class="{},{}">
            <i>
                <slot name="icon"></slot>
            </i>
            <slot name="text"></slot>
        </button>
    </div>
</template>

<script>
    export default {
      name: 'custom-button' ,
       props: {
            type: {
                type: String,
                default: 'button',
                validator: (value) => {
                    return [
                        'link',
                        'button'
                    ].indexOf(value) >=0
                }
            },
            color: {
                type: String,
                validator: (value) => {
                    return [
                        'primary',
                        'secondary',
                        'warning',
                        'disabled',
                        'info',
                        'danger',
                        'action'
                    ].indexOf(value) >=0
                }
            },
            size: {
                type: String,
                default: 'normal',
                validator: (value) => {
                    return [
                        'small',
                        'normal'
                    ].indexOf(value) >=0
                }
            },
            timer: {

            },
            disabeled: {
                type: Boolean
            }
       },
       computed: {
        listClasses() {
            return [
                
            ]
        }
       }
    }
</script>

<style lang="scss" scoped>

</style>