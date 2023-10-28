<script setup lang="ts">
import TheHeader from "@/components/TheHeader.vue";
import EntryEditor from "./components/EntryEditor.vue";
import EntryCard from "@/components/EntryCard.vue";

import { reactive } from "vue";

interface User {
  id: number;
  username: string;
  settings: string[];
}

const user = reactive({
  id: 1,
  username: "ajukadavid",
  settings: [] as string[],
});
</script>

<template>
  <main class="container m-auto p-10">
    <TheHeader />
    <EntryEditor />
    <ul>
      <li>
        <EntryCard />
      </li>
    </ul>
  </main>
</template>
