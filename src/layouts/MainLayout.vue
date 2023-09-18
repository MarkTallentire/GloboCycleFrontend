<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-toolbar-title>
          Globo Cycle
        </q-toolbar-title>

      </q-toolbar>

      <q-tabs v-model="tab">
        <q-tab v-for="link in links" :name="link.name" :label="link.name" :key="link.name"
          @click="router.push(link.link)" />
      </q-tabs>

    </q-header>

    <q-page-container>
      <router-view class="q-mt-md" />
    </q-page-container>
  </q-layout>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import { useRouter } from 'vue-router';

const router = useRouter();

const tab = ref('events')

const links = [
  {
    name: "events",
    link: "/"
  },
  {
    name: "New Event",
    link: "/newevent"
  }
]

</script>
