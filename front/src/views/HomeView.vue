<script setup lang="ts">
import type { Photography } from "@/photography";
import TheCard from "../components/TheCard.vue";
const photographys: Array<Photography> = [
  {
    characteristics: [
      "Drone Photography ",
      "Interiors",
      "Exteriors / Architectural",
    ],
    title: "Photography",
    description:
      "Every photograph we produce finds the beauty in your property while serving as a profitable asset.",
    images: ["/photograpy/img/photo1.png", "/photograpy/img/photo2.png"],
    id: 1,
  },
  {
    title: "Virtual Staging",
    description: `Our staging will help you sell the potential of your space.
We can work off of our own photography or photos you provide.`,
    images: ["/photograpy/img/photo4.png"],
    id: 2,
  },
  {
    characteristics: ["Interiors ", "Exteriors"],
    title: "Renderings",
    description:
      "Renderings are the gold standard in pre-construction marketing.",
    images: ["/photograpy/img/photo7.png"],
    id: 3,
  },
  {
    characteristics: ["Matterport", "Video Walkthroughs"],
    title: "Interactive Tours",
    description:
      "Give your audience the ability to explore your property without requiring in-person travel.",
    images: ["/photograpy/img/photo3.png"],
    id: 4,
  },
  {
    characteristics: ["On-site Measure", "2D Floor Plans", "3D Floor Plans"],
    title: "Floor Plans",
    description:
      "We produce laser-precise floor plans faster than any other service.",
    images: ["/photograpy/img/photo5.png"],
    id: 5,
  },
  {
    characteristics: [
      "Drone Cinematography",
      "Interiors",
      "Exteriors / Architectural",
    ],
    title: "Video",
    description:
      "Video content has higher engagement and will help your property stand out online.",
    images: ["/photograpy/img/photo6.png"],
    id: 6,
  },
];
</script>

<template>
  <header>
    <h1>
      We make creative media <br />
      that <span> adds value</span>
    </h1>
  </header>
  <main>
    <section>
      <TheCard
        :key="photo.id"
        :photography="photo"
        v-for="photo in photographys"
      >
      </TheCard>
    </section>
    <div class="buttom">
      <button>Get STARTED</button>
    </div>
  </main>
</template>

<style scoped>
section {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(min(100%, 30rem), 1fr));
  grid-auto-flow: dense;
  gap: 2.6rem;
}

.buttom {
  text-align: center;
  margin: 2rem 0 3rem;
}
button {
  padding: 1rem 3rem;
  text-transform: uppercase;
  background: #1b264f;
  border-radius: 12px;
  color: white;
  font-family: "Poppins";
  font-style: normal;
  font-weight: 700;
  border: none;
  letter-spacing: 0.2rem;
}

header {
  margin-top: 4rem;
}

h1 {
  font-family: "Poppins";
  text-align: center;
  font-style: normal;
  font-weight: 700;
  letter-spacing: -0.01rem;
  font-size: 3.7rem;
}

h1 span {
  color: #506bca;
  font-weight: 800;
}
</style>
