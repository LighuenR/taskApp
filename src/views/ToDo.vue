<template>
    <v-card>
        <v-text-field
            label="Append inner"
            append-inner-icon="mdi-map-marker"
            variant="solo"
          ></v-text-field>
          <v-divider></v-divider>
        <v-list select-strategy="classic" class="pa-0">
            <div v-for="task in tasks" :key="task.id">
                <v-list-item @click="doneTask(task.id)" :class="{ 'blue': task.done }">
                    <template v-slot:prepend>
                        <v-list-item-action start>
                            <v-checkbox-btn :model-value="task.done"></v-checkbox-btn>
                        </v-list-item-action>
                        
                    </template>
                    <v-list-item-title :class="{ ' text-decoration-line-through': task.done }">
                        {{ task.title }}
                    </v-list-item-title>
                    <template v-slot:append>
                        <v-btn @click="deleteTask(task.id)" color="black" icon="mdi-delete" variant="text"></v-btn>
                    </template>
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
                    title: 'Wake up',
                    done: false
                },
                {
                    id: 2,
                    title: 'Study vue and vuetify',
                    done: false
                },
                {
                    id: 3,
                    title: 'Clean the house',
                    done: false
                }
            ]
        }


    },
    methods: {

        doneTask(id) {
            let task = this.tasks.filter(task => task.id === id)[0]
            task.done = !task.done
        },
        deleteTask(id) {
           this.tasks = this.tasks.filter(task => task.id !== id)
        }
    }
}
</script>

<style scoped>
.blue {
    background: rgb(195, 195, 195)
}
</style>