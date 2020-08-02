<template>
  <div class="the-heading-title">
    <v-card class="pl-4 pt-4 pr-4 pb-4">
      <span>{{title}}</span>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "TheHeadingTitle",
  props: {
      title: {
          type: String,
          default: "Title in not available"
      },
  },
};
</script>

