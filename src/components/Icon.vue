<template>
    <div>
        <v-icon v-if="nameIcon == 'open'">mdi-open-in-new</v-icon>
        <v-icon v-if="nameIcon == 'delete'">mdi-delete</v-icon>
        <v-icon v-if="nameIcon == 'edit'">mdi-edit</v-icon>
        <v-icon v-if="nameIcon == 'add'">mdi-account-multiple-plus</v-icon>
        <v-icon v-if="nameIcon == 'clear'">mdi-broom</v-icon>
        <v-icon v-if="nameIcon == 'loading'">mdi-loading</v-icon>
        <v-icon v-if="nameIcon == 'draw'">mdi-shuffle-variant</v-icon>
    </div>
</template>

<script>
export default {
    name: 'Icon',
    props: {
        nameIcon: String,
        rotate: Boolean || undefined,
    },
}
</script>