<template>
  <div>
    <Navbar />
    <router-view />
    <Foot />
  </div>
</template>

<script>
import Navbar from "@/components/Navbar";
import Foot from "@/components/Foot";
export default {
  components: {
    Navbar,
    Foot
  }
};
</script>
