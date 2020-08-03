<template>
  <v-container>
    <v-row>
      <v-col cols="12">
        <TheHeadingTitle title="Developing Card" />
      </v-col>
    </v-row>
    <v-row>
      <v-col md="3" v-for="item in card_example" :key="item.title">
        <KCard03 :img-url="item.url" :img-title="item.title" />
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <TheHeadingTitle title="KCard 01" />
      </v-col>
    </v-row>
    <v-row>
      <v-col md="3" v-for="item in card_example" :key="item.title">
        <KCard01 :img-url="item.url" :img-title="item.title" />
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <TheHeadingTitle title="KCard 02" />
      </v-col>
    </v-row>
    <v-row>
      <v-col md="3" v-for="item in card_example" :key="item.title">
        <KCard02 :img-url="item.url" :img-title="item.title" />
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12">
        <TheHeadingTitle title="KCard 03" />
      </v-col>
    </v-row>
    <v-row>
      <v-col md="3" v-for="item in card_example" :key="item.title">
        <KCard03 :img-url="item.url" :img-title="item.title" />
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import KCard01 from "../components/KCard01";
import KCard02 from "../components/KCard02";
import KCard03 from "../components/KCard03";
import TheHeadingTitle from "../components/TheHeadingTitle";

export default {
  name: "card",
  components: {
    KCard01,
    KCard02,
    KCard03,
    TheHeadingTitle
  },
  data() {
    return {
      card_example: [
        {
          url:
            "https://upload.wikimedia.org/wikipedia/commons/2/25/Logo_kmitl.png",
          title: "Title1"
        },
        {
          url:
            "https://upload.wikimedia.org/wikipedia/commons/2/25/Logo_kmitl.png",
          title: "Title2"
        },
        {
          url:
            "https://upload.wikimedia.org/wikipedia/commons/2/25/Logo_kmitl.png",
          title: "Title3"
        },
        {
          url:
            "https://upload.wikimedia.org/wikipedia/commons/2/25/Logo_kmitl.png",
          title: "Title4"
        }
      ]
    };
  }
};
</script>
