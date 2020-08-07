<template>
  <v-container>
    <v-row>
      <v-col cols="12">
          <TheHeadingTitle title="Developing Button"/>
      </v-col>
    </v-row>
    <v-row>
        <v-col cols="3" v-for="(item, index) in button_example" :key="index" class="d-flex justify-center">
            <KButton01 :text="item.text" @btnClick="handleButtonClick"/>
        </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
          <TheHeadingTitle title="KButton1"/>
      </v-col>
    </v-row>
    <v-row>
        <v-col cols="3" v-for="(item, index) in button_example" :key="index" class="d-flex justify-center">
            <KButton01 :text="item.text"/>
        </v-col>
    </v-row>
  </v-container>
</template>

<script>
import TheHeadingTitle from "../components/TheHeadingTitle";
import KButton01 from '../components/KButton01';

export default {
  name: "button",
  components: {
      TheHeadingTitle,
      KButton01,
  },
  data() {
      return {
          button_example: [
              {
                  text: "Button1"
              },
              {
                  text: "Button2"
              },
              {
                  text: "Button3"
              },
              {
                  text: "Button4"
              },
          ]
      }
  },
  methods: {
      handleButtonClick() {
          console.log("KButtonClicked!");
      }
  },
};
</script>

<style lang="scss" scoped>
</style>