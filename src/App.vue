<script >
import CustomButton from '@/components/CustomButton.vue'
import IconArrowGreater from './components/icons/IconArrowGreater.vue';
export default{
  components: {
    CustomButton,
    IconArrowGreater
}
}
</script>

<template>
  <main>
    <custom-button success><IconArrowGreater/></custom-button>
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  * {
    margin: 0;
    padding: 0;
  }
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
