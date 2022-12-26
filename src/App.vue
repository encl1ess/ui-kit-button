<script >
import CustomButton from '@/components/CustomButton.vue'
import IconArrowGreater from './components/icons/IconArrowGreater.vue';
import IconExit from './components/icons/IconExit.vue';
import IconVK from './components/icons/IconVK.vue';
export default {
  components: {
    CustomButton,
    IconArrowGreater,
    IconExit,
    IconVK
}
}
</script>

<template>
  <main>
    <custom-button success><IconVK/> Повторное письмо</custom-button>
    <custom-button success type="link" url="#">Link </custom-button>
  </main>
</template>

<style >
* {
  margin: 0;
  padding: 0;
}

body {
  background: #1E1E1E;
}

#app {
    margin: 1em;
}
</style>
