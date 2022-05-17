<template>
    <v-form class="hello">
      <h1>Yup SandBox</h1>

      <v-text-field
          v-model="root['myField']['question']"
      />

      {{ errors }}
      <br />

      <br />
      {{ myField }}
    </v-form>
</template>

<script setup>
import { useForm, useField } from 'vee-validate';
import { ref } from 'vue';
import { buildYup } from 'schema-to-yup';

const schema = {
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "properties": {
    "myField": {
      "oneOf": [
        {"const": "value1"},
        {"const": "value2"}
      ]
    }
  }
}
const root = ref({});

const { errors } = useForm(
    {
      validationSchema: buildYup(schema, {})
    }
);
const { value } =  useField(
    'myField',
    undefined,
);
root.value['myField'] = value;
root.value['myField'] = {};

</script>
