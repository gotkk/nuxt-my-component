<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <TheHeadingTitle title="Card Hover Effect 01"/>
      </v-col>
    </v-row>
    <v-row>
      <v-col md="3" v-for="item in card_example" :key="item.title">
        <KCard01 :img-url="item.url" :img-title="item.title" />
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
          <TheHeadingTitle title="Card Hover Effect 02" />
      </v-col>
    </v-row>
    <v-row>
      <v-col md="3" v-for="item in card_example" :key="item.title">
        <KCard02 :img-url="item.url" :img-title="item.title" />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import KCard01 from "../components/KCard01";
import KCard02 from "../components/KCard02";
import TheHeadingTitle from "../components/TheHeadingTitle"

export default {
  name: "card",
    components: {
    KCard01,
    KCard02,
    TheHeadingTitle,
  },
  data() {
    return {
      card_example: [
        {
          url:
            "https://th-test-11.slatic.net/p/6932df14abb539d76b9dc01edaf5e8f9.jpg_340x340q80.jpg_.webp",
          title: "Product1"
        },
        {
          url:
            "https://th-test-11.slatic.net/p/6932df14abb539d76b9dc01edaf5e8f9.jpg_340x340q80.jpg_.webp",
          title: "Product2"
        },
        {
          url:
            "https://th-test-11.slatic.net/p/6932df14abb539d76b9dc01edaf5e8f9.jpg_340x340q80.jpg_.webp",
          title: "Product3"
        },
        {
          url:
            "https://th-test-11.slatic.net/p/6932df14abb539d76b9dc01edaf5e8f9.jpg_340x340q80.jpg_.webp",
          title: "Product4"
        }
      ]
    };
  },
};
</script>
