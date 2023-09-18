<template>
    <q-card v-for='event in events' :key='event.name' class='my-card' flat bordered>
        <q-card-section horizontal>
            <q-card-section class='q-pt-xs'>
                <div class='text-overline'>{{ event.type }}</div>
                <div class='text-h5 q-mt-sm q-mb-xs'>{{ event.name }}</div>
                <div class='text-caption text-grey'>
                    {{ event.body }}
                </div>
            </q-card-section>

            <q-card-section class='col-5 flex flex-center'>
                <q-img class='rounded-borders' src='https://cdn.quasar.dev/img/parallax2.jpg' />
            </q-card-section>
        </q-card-section>

        <q-separator />

        <q-card-actions class="row items-center">

            <q-btn flat round icon='event' />
            <q-btn flat>
                {{ event.time }}
            </q-btn>

        </q-card-actions>

    </q-card>
</template>

<script setup lang="ts">
defineProps<{
    events: { id: number; type: string; name: string; body: string; time: string; }[];
}>()
</script>
