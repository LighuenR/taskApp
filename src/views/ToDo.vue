<template>

        <v-card>
            <v-list select-strategy="classic">
                <div v-for="task in tasks" :key="task.id">
                    <v-list-item >
                        <template v-slot:prepend="{ isActive }">
                            <v-list-item-action start>
                                <v-checkbox-btn :model-value="isActive"></v-checkbox-btn>
                            </v-list-item-action>
                        </template>
                        <v-list-item-title>{{ task.title }}</v-list-item-title>
                    </v-list-item>
                    <v-divider></v-divider>
                </div>
            </v-list>
        </v-card>
 
</template>

<script>
export default {
    data() {
        return {
            tasks: [
                {
                    id: 1,
                    title: 'Wake up'
                },
                {
                    id: 2,
                    title: 'Study vue and vuetify'
                },
                {
                    id: 3,
                    title: 'Clean the house'
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped></style>