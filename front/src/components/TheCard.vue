<script setup lang="ts">
import type { PropType } from "vue";
import type { Photography } from "../photography";

defineProps({
  photography: { type: Object as PropType<Photography>, required: true },
});
</script>

<template>
  <div class="card">
    <div class="left">
      <img
        :key="`${photography.title}-${index}`"
        v-for="(image, index) in photography.images"
        :src="image"
        alt="Not found"
      />
    </div>
    <div class="right">
      <h2>{{ photography.title }}</h2>
      <ul>
        <li
          :key="characteristic"
          v-for="characteristic in photography.characteristics"
        >
          {{ characteristic }}
        </li>
      </ul>
      <p :key="line" v-for="line in photography.description.split('\n')">
        {{ line }}
      </p>
    </div>
  </div>
</template>

<style scoped>
h2 {
  font-family: "Poppins";
  font-style: normal;
  font-weight: 700;
}
.card {
  border-radius: 8px;
  display: flex;
  font-family: "Nunito Sans";
}
.card .left {
  width: 100%;
  display: flex;
  flex-direction: column;
  border-radius: 8px;
}

.card .right {
  width: 100%;
  padding: 1rem;
  background: white;
}

li::marker {
  color: #d2ad81;
}
li {
  font-weight: 600;
}

ul {
  padding-left: 1rem;
}
.left img {
  width: 100%;
  height: 100%;
}

.left img:first-child {
  border-radius: 8px 0 0 0;
}

.left img:last-child {
  border-radius: 0 0 0 8px;
}
</style>
