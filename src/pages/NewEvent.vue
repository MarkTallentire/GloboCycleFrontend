<template>
    <q-page>
        <div style="display: flex; justify-content: center; width: 100%;">
            <div class="q-pa-md" style="display: flex; justify-content:center">
                <q-form class="q-gutter-md" style="width: 1200px;" @submit="onSubmit">
                    <p>Create a new event</p>
                    <q-input v-model="name" placeholder="Name" outlined />
                    <q-input v-model="type" placeholder="Type" outlined />
                    <q-input type="textarea" cols="20" rows="20" v-model="body" placeholder="Body" outlined />
                    <q-input v-model="time" placeholder="Time" outlined />

                    <q-btn type="submit" color="positive">Submit</q-btn>
                </q-form>
            </div>
        </div>
    </q-page>
</template>
  
<script setup lang='ts'>
import { ref } from 'vue';

const name = ref('');
const type = ref('');
const body = ref('')
const time = ref('')

const onSubmit = (e: any) => {
    alert(name.value + type.value + body.value + time.value)
}


</script>
  