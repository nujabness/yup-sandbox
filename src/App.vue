<template>
  <v-app>
    <v-main>
<!--      <schema-one-of-string/>-->
<!--      <schema-any-of-required/>-->
      <schema-one-of-object/>
    </v-main>
  </v-app>
</template>

<script>
// import schemaOneOfString from "@/components/schemaOneOfString";
// import schemaAnyOfRequired from "@/components/schemaAnyOfRequired";
import schemaOneOfObject from "@/components/schemaOneOfObject";

export default {
  name: 'App',

  components: {
    // schemaOneOfString,
    // schemaAnyOfRequired,
    schemaOneOfObject,
  },

  data: () => ({
    //
  }),
}
</script>
