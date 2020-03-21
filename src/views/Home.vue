<template>
  <div class="home">
    <div class="home">
      <MyButton
        :greet="greetText"
        @click="onMyButtonClicked"
      >
      </MyButton>
    </div>
  </div>
</template>

<script lang="ts">
// @ is an alias to /src
  import {Component, Vue} from "vue-property-decorator";
  import MyButton from "@/components/MyButton.vue";

  @Component({
    components: {
      MyButton,
    },
  })

  export default class Home extends Vue {
    public greetText = "Hello";

    public onMyButtonClicked() {
      this.greetText = "こんにちは";
    }
  }
</script>
