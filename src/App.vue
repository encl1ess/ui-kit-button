<script >
import CustomButton from '@/components/CustomButton.vue'
export default {
  components: {
    CustomButton,
  }
}
</script>

<template>
  <main class="flex-container flex-container_row">
    <div class="flex-container flex-container_column">

      <custom-button success type="link" url="#">Link </custom-button>
      <custom-button success timer="02:00"></custom-button>
    </div>
    <div class="flex-container flex-container_column">
   
    </div>
    <div class="flex-container flex-container_column">
      <custom-button primary>
        <iarrow/>
      </custom-button>
      <custom-button primary>
        <iquest />
      </custom-button>
    </div>

  </main>
</template>

<style lang="scss">
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

.flex-container {
  display: flex;
  align-items: center;

  &_column {
    flex-direction: column;
  }
}
</style>
