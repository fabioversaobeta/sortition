<template>
  <div>
    <v-text-field v-if="typeInput == 'required'"
      :label="label"
      :rules="rules"
      hide-details="auto"
      v-model="valueField"
    ></v-text-field>

    <v-text-field v-else-if="typeInput == 'normal'" 
        label="Another input" 
        v-model="valueField"
    ></v-text-field>
  </div>
</template>

<script>
export default {
    name: 'Input',
    props: {
        label: String,
        typeInput: String,
    },
    data() {
        return {
            rules: [
                value => !!value || 'Obrigatório.',
                value => (value && value.length >= 3) || 'Min. 3 letras',
            ],
            valueField: '',
        }
    },
}
</script>