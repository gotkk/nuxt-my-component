<template>
  <v-container>
    <v-row>
      <v-col md="3" v-for="item in card_hover01" :key="item.title">
        <CardHover01 :img-url="item.url" :img-title="item.title" />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import CardHover01 from "../components/CardHover01";
export default {
  name: "card",
  data() {
    return {
      card_hover01: [
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
  components: {
    CardHover01
  }
};
</script>
