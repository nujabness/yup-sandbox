<template>
    <v-form class="hello">
      <h1>Yup SandBox</h1>

<!--      <v-select-->
<!--          v-model="root['myField']"-->
<!--          :items="items"-->
<!--          multiple-->
<!--      />-->
<!--&lt;!&ndash;      <v-text-field&ndash;&gt;-->
<!--&lt;!&ndash;          v-model="root['otherInvestmentSource']"&ndash;&gt;-->
<!--&lt;!&ndash;      />&ndash;&gt;-->

<!--      {{ errors }}-->
<!--      <br />-->

<!--      <br />-->
<!--      {{ myField }}-->
    </v-form>
</template>

<script setup>
// import { useForm, useField } from 'vee-validate';
// import { ref } from 'vue';
// import { buildYup } from 'schema-to-yup';
import convertToYup from "json-schema-yup-transformer";
// const schema = {
//     "$schema": "http://json-schema.org/draft-07/schema",
//     "type": "object",
//     "properties": {
//     "required": ["user"],
//     "user": {
//       "type": "array",
//       "items": {
//         "type": "string",
//         "enum": ["foo", "bar"]
//       }
//     },
//     "admin": {
//       "type": "string"
//     }
//   },
//   "if": {
//     "properties": {
//       "user": {
//         "contains": {
//           "type": "string",
//               "const": "foo"
//         }
//       }
//     }
//   },
//   "then": {
//     "required": ["admin"]
//   },
// }

const schema = {
  type: "object",
  $schema: "http://json-schema.org/draft-07/schema",
  $id: "example",
  title: "Example",
  properties: {
    name: {
      type: "string"
    }
  }
};
//
// const root = ref({});
// const items = [
//   { title: "1", value: "value1" },
//   { title: "2", value: "value2" },
//   { title: "3", value: "value3" }
// ];
//
const schemaYup = convertToYup(schema)
// console.log("JFDNKSJFKSJHDBFK")
console.log(schemaYup)
// const { errors } = useForm({ validationSchema: schemaYup});
// console.log("99999999999999999")
// const { value } =  useField(
//     'myField',
//     undefined
// );
// root.value['myField'] = value;
// root.value['myField'] = {};

</script>
