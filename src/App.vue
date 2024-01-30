<script setup>
import { ref } from 'vue'
const newGroup = ref({
  section: '',
  groupName: '',
  repo: '',
  members: []
})
const numOfMembers = ref(0)
</script>

<template>
  <div class="w-full">
    <div class="flex flex-col gap-2 bg-slate-100 p-3">
      <div>
        Section:
        <select v-model="newGroup.section">
          <option value="1">1</option>
          <option value="1">2</option>
        </select>
        {{ newGroup.section }}
      </div>
      <div>
        Group Name:
        <input
          type="text"
          v-model.trim="newGroup.groupName"
          class="w-1/2 border border-gray-300 p-0.5 outline-none rounded-lg"
        />
        {{ newGroup.groupName }}
      </div>
      <div>
        GitHub Repository:
        <input
          type="text"
          v-model.trim="newGroup.repo"
          class="w-1/2 border border-gray-300 p-0.5 outline-none rounded-lg"
        />
        {{ newGroup.repo }}
      </div>
      <div>
        <div>
          Number of Members:
          <input
            type="number"
            min="0"
            v-model.number="numOfMembers"
            class="border border-gray-300 p-0.5 outline-none rounded-lg"
          />
          {{ numOfMembers }}
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
</style>