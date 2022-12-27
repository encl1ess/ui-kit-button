<script >
import CustomButton from '@/components/CustomButton.vue'
import IconVk from './components/icons/IconVk.vue';
export default {
  components: {
    CustomButton,
    IconVk
}
}
</script>

<template>
  <main class="flex-container flex-container__row">
    <div class="flex-container flex-container__column">
      <p class="flex-container__title"> (button link)</p>
      <custom-button success type="link" url="#1">Напомнить PIN-код</custom-button>
      <custom-button success type="link" url="#">Напомнить PIN-код</custom-button>
    </div>
    <div class="flex-container flex-container__column">

    </div>
    <div class="flex-container flex-container__column">
      <p class="flex-container__title"> (button multi-sized)</p>
      <div class="flex-container flex-container__row">
        <p>mobile</p>
        <p>desktop</p>
      </div>
      <div class="flex-container flex-container__row">
        <custom-button icon primary small>
          <iarrow />
        </custom-button>
        <custom-button icon primary>
          <iarrow />
        </custom-button>
      </div>
      <div class="flex-container flex-container__row">
        <custom-button icon danger small>
          <iexit />
        </custom-button>
        <custom-button icon danger>
          <iexit />
        </custom-button>
      </div>
      <div class="flex-container flex-container__row">
        <custom-button icon success small>
          <iquest />
        </custom-button>
        <custom-button icon success>
          <iquest />
        </custom-button>
      </div>

      <div class="flex-container flex-container__row">
        <custom-button icon primary small>
          <iarrow-greater />
        </custom-button>
        <custom-button icon primary>
          <iarrow-greater />
        </custom-button>
      </div>
      <div class="flex-container flex-container__row">
        <custom-button icon danger small>
          <igoogle />
        </custom-button>
        <custom-button icon danger>
          <igoogle />
        </custom-button>
      </div>
      <div class="flex-container flex-container__row">
        <custom-button icon info small>
          <ivk />
        </custom-button>
        <custom-button icon info>
          <ivk />
        </custom-button>
      </div>
      <div class="flex-container flex-container__row">
        <custom-button icon action small>
          <iclass />
        </custom-button>
        <custom-button icon action>
          <iclass />
        </custom-button>
      </div>
      <div class="flex-container flex-container__row">
        <custom-button icon primary small>
          <ipen />
        </custom-button>
        <custom-button icon primary>
          <ipen />
        </custom-button>
      </div>
    </div>
    <div class="flex-container flex-container__column">
      <p class="flex-container__title"> (button timer)</p>
      <p>(disabled)</p>  
      <custom-button disabled timer="2:00">
         Повторное письмо
      </custom-button>
    </div>
    <div class="flex-container flex-container__column">
      <p class="flex-container__title"> (button classic)</p>
      <p>(primary)</p>  
      <custom-button primary>
         Оправить письмо
      </custom-button>
      <p>(secondary)</p>  
      <custom-button secondary>
         Оправить письмо
      </custom-button>
      <p>(warning)</p>  
      <custom-button warning>
         Оправить письмо
      </custom-button>
      <p>(disabled)</p>  
      <custom-button disabled>
         Оправить письмо
      </custom-button>
      <p>(info)</p>  
      <custom-button info>
         Оправить письмо
      </custom-button>
      <p>(danger)</p>  
      <custom-button danger>
         Оправить письмо
      </custom-button>
      <p>(action)</p>  
      <custom-button action>
         Оправить письмо
      </custom-button>
    </div>

    <div class="flex-container flex-container__column">
      <p class="flex-container__title"> (other)</p>
      <p>(primary)</p>  
      <custom-button primary>
         Повторное письмо
      </custom-button>
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
  font-weight: 700;
}

body {
  background: #1E1E1E;
}


#app {
  margin: 1em;
}

.flex-container {
  margin: 0.5em;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
  gap: 10px;
  &:first-child {
    align-items: flex-start;
  }

  &__title {
    text-transform: uppercase;
    align-self: center;
    font-weight: 1000;
    color: #C8C8C8;
  }

  &__column {
    flex-direction: column;
  }
}
</style>
