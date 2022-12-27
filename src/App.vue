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
      <p style="text-transform: uppercase;"> (button multi-sized)</p>
      <div class="flex-container flex-container_row">
        <p>mobile</p>
        <p>desktop</p>
      </div>
      <div class="flex-container flex-container_row">
        <custom-button primary small>
          <iarrow />
        </custom-button>
        <custom-button primary>
          <iarrow />
        </custom-button>
      </div>
      <div class="flex-container flex-container_row">
        <custom-button danger small>
          <iexit />
        </custom-button>
        <custom-button danger>
          <iexit />
        </custom-button>
      </div>
      <div class="flex-container flex-container_row">
        <custom-button success small>
          <iquest />
        </custom-button>
        <custom-button success>
          <iquest />
        </custom-button>
      </div>

      <div class="flex-container flex-container_row">
        <custom-button primary small>
          <iarrow-greater />
        </custom-button>
        <custom-button primary>
          <iarrow-greater />
        </custom-button>
      </div>
      <div class="flex-container flex-container_row">
        <custom-button danger small>
          <igoogle />
        </custom-button>
        <custom-button danger>
          <igoogle />
        </custom-button>
      </div>
      <div class="flex-container flex-container_row">
        <custom-button info small>
          <ivk />
        </custom-button>
        <custom-button info>
          <ivk />
        </custom-button>
      </div>
      <div class="flex-container flex-container_row">
        <custom-button action small>
          <iclass />
        </custom-button>
        <custom-button action>
          <iclass />
        </custom-button>
      </div>
      <div class="flex-container flex-container_row">

      </div>
      <div class="flex-container flex-container_row">
        <custom-button primary small>
          <ipen />
        </custom-button>
        <custom-button primary>
          <ipen />
        </custom-button>
      </div>
    </div>

  </main>
</template>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  font-family: 'Nunito';
  text-align: center;
  color: #ffffff;
}
p {
  margin: 0.5em 1em;
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
