<template>
    <div>
        <div>Lista</div>
        <Input :label="'Nome'" :typeInput="'required'" :changeValue="changeValue"/>
        <Button :title="'Add'" :icon="'add'" />
        <ul v-for="item in items" :key="item.id">
            <li>
                {{ item.name }} - <Button :title="'Remove'" :icon="'delete'" /> <Button :title="'Edit'" :icon="'edit'" />
            </li>
        </ul>
        <Button :title="'Clear'" :icon="'clear'" />

        <hr />

        <Button :title="'Draw'" :icon="'draw'" />

        [ SHOW DRAWED]

    </div>
</template>

<script>
import Button from '@/components/Button.vue'
import Input from '@/components/Input.vue'

export default {
    name: 'Lista',
    components: {
        Button,
        Input,
    },
    data() {
        return {
            inputValue: '',
            items: [
                {
                    id: 1,
                    name: 'Item 1'
                },
                {
                    id: 2,
                    name: 'Item 2'
                },
                {
                    id: 3,
                    name: 'Item 3'
                },
                {
                    id: 4,
                    name: 'Item 4'
                },
            ],
        }
    },
    methods: {
        changeValue: function (value) {
            this.inputValue = value
        },
    },
}
</script>